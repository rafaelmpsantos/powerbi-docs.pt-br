---
title: Filtragem cruzada bidirecional no Power BI Desktop (Preview)
description: Habilitar a filtragem cruzada usando o DirectQuery no Power BI Desktop
services: powerbi
documentationcenter: 
author: davidiseminger
manager: kfile
backup: 
editor: 
tags: 
qualityfocus: no
qualitydate: 
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 09/06/2017
ms.author: davidi
ms.openlocfilehash: 7946a9389897c4401e581482c0630547a764616d
ms.sourcegitcommit: 284b09d579d601e754a05fba2a4025723724f8eb
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/15/2017
---
# <a name="bidirectional-cross-filtering-using-directquery-in-power-bi-desktop-preview"></a>Filtragem cruzada bidirecional usando o DirectQuery no Power BI Desktop (Preview)

Ao filtrar tabelas para criar a exibição de dados apropriada, os criadores de relatório (e modeladores de dados) enfrentam desafios ao determinar como a filtragem é aplicada a um relatório; o contexto de filtro de uma tabela foi mantido em um lado da relação, mas não no outro, exigindo, muitas vezes, fórmulas DAX complexas para obter os resultados desejados.

Com a filtragem cruzada bidirecional, os criadores de relatório (e modeladores de dados) agora têm mais controle sobre como os filtros são aplicados ao trabalhar com tabelas relacionadas, permitindo que eles sejam aplicados em *ambos* os lados de uma relação de tabela. Isso é realizado com a propagação do contexto de filtro em uma segunda tabela relacionada do outro lado de uma relação de tabela.

Um [white paper detalhado](http://download.microsoft.com/download/2/7/8/2782DF95-3E0D-40CD-BFC8-749A2882E109/Bidirectional%20cross-filtering%20in%20Analysis%20Services%202016%20and%20Power%20BI.docx) que explica a filtragem cruzada bidirecional no Power BI Desktop está disponível (também aborda o SQL Server Analysis Services 2016, que tem o mesmo comportamento).

* Baixar o white paper [Bidirectional cross-filtering for Power BI Desktop](http://download.microsoft.com/download/2/7/8/2782DF95-3E0D-40CD-BFC8-749A2882E109/Bidirectional%20cross-filtering%20in%20Analysis%20Services%202016%20and%20Power%20BI.docx) (Filtragem cruzada bidirecional para o Power BI Desktop)

### <a name="enabling-bidirectional-cross-filtering-for-directquery"></a>Habilitando a filtragem cruzada bidirecional para o DirectQuery
Para usar a filtragem cruzada para o DirectQuery, primeiro você deve habilitá-la. Esse é um recurso de preview, o que significa que sua disponibilidade e seu comportamento estão sujeitos a alterações em versões futuras do Power BI Desktop.

Para habilitar a filtragem cruzada para o DirectQuery no Power BI Desktop, selecione **Arquivo > Opções e Configurações > Opções**, marque a caixa ao lado de **Habilitar filtragem cruzada em ambas as direções para o DirectQuery**, conforme mostrado na imagem a seguir.

![](media/desktop-bidirectional-filtering/bidirectional-filtering_1.png)

> [!NOTE]
> Ao criar fórmulas DAX de filtragem cruzada no Power BI Desktop, use *UserPrincipalName* (que é geralmente o mesmo logon do usuário, como *joe@contoso.com*), em vez de *UserName*. Assim, você poderá precisar criar uma tabela relacionada que mapeia *UserName* (ou EmployeeID, por exemplo) para *UserPrincipleName*.
> 
> 

Para habilitar a filtragem cruzada, na caixa de diálogo **Editar Relação** de uma relação, selecione o seguinte:

* A **Direção do filtro cruzado** deve ser definida como **Ambos**
* A opção **Aplicar filtro de segurança em ambas as direções** também deve ser selecionada
  
  ![](media/desktop-bidirectional-filtering/bidirectional-filtering_2.png)

Para obter mais informações e exemplos de como funciona a filtragem cruzada bidirecional, confira o [white paper](http://download.microsoft.com/download/2/7/8/2782DF95-3E0D-40CD-BFC8-749A2882E109/Bidirectional%20cross-filtering%20in%20Analysis%20Services%202016%20and%20Power%20BI.docx) mencionado anteriormente neste artigo.
