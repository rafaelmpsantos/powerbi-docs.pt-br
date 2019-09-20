---
title: Pré-requisitos de fonte de dados do Power BI
description: Pré-requisitos de fonte de dados do Power BI
author: davidiseminger
manager: kfile
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-desktop
ms.topic: conceptual
ms.date: 05/08/2019
ms.author: davidi
LocalizationGroup: Connect to data
ms.openlocfilehash: 5a95607c2328115df7b4485756f40340a8cb7b0f
ms.sourcegitcommit: 60dad5aa0d85db790553e537bf8ac34ee3289ba3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "65454393"
---
# <a name="power-bi-data-source-prerequisites"></a>Pré-requisitos de Fonte de Dados do Power BI
Para cada provedor de dados, o Power BI dá suporte a uma versão específica do provedor em objetos. Para obter mais informações sobre as fontes de dados disponíveis para o Power BI, veja [Fontes de dados](desktop-data-sources.md). A tabela a seguir descreve esses requisitos.

| Fonte de dados | Provedor | Versão mínima do provedor | Versão mínima da fonte de dados | Objetos de fonte dados com suporte | Link de download |
| --- | --- | --- | --- | --- | --- |
| SQL Server |ADO.net (interno no .Net Framework) |.NET Framework 3.5 (somente) |SQL Server 2005+ |Tabelas/modos de exibição, Funções escalares, Funções de tabela |Incluído no .NET Framework 3.5 ou superior |
| Access |Mecanismo de Banco de Dados do Microsoft Access (ACE) |ACE 2010 SP1 |Nenhuma restrição |Tabelas/modos de exibição |[Link de download](http://go.microsoft.com/fwlink/?linkid=285987&clcid=0x409) |
| Excel (somente arquivos .xls) (veja a observação 1) |Mecanismo de Banco de Dados do Microsoft Access (ACE) |ACE 2010 SP1 |Nenhuma restrição |Tabelas, planilhas |[Link de download](http://go.microsoft.com/fwlink/?linkid=285987&clcid=0x409) |
| Oracle (consulte a observação 2) |ODP.NET |ODAC 11.2 versão 5 (11.2.0.3.20) |9.x+ |Tabelas/modos de exibição |[Link de download](http://go.microsoft.com/fwlink/?linkid=272376&clcid=0x409) |
| | System.Data.OracleClient (criado no .NET Framework) |.NET Framework 3.5 |9.x+ |Tabelas/modos de exibição |Incluído no .NET Framework 3.5 ou superior |
| IBM DB2 |Cliente ADO.Net da IBM (parte do pacote de driver do servidor de dados da IBM) |10.1 |9.1+ |Tabelas/modos de exibição |[Link de download](http://go.microsoft.com/fwlink/?linkid=274911&clcid=0x409) |
| MySQL |Conector/rede |6.6.5 |5.1 |Tabelas/modos de exibição, Funções escalares |[Link de download](https://dev.mysql.com/downloads/connector/net/6.10.html) |
| PostgreSQL |Provedor ADO.NET NPGSQL |2.0.12 |7.4 |Tabelas/modos de exibição |[Link de download](http://go.microsoft.com/fwlink/?linkid=282716&clcid=0x409) |
| Teradata |Provedor de dados .Net para Teradata |14+ |12+ |Tabelas/modos de exibição |[Link de download](http://go.microsoft.com/fwlink/?linkid=278886&clcid=0x409) |
| SAP Sybase SQL Anywhere |iAnywhere.Data.SQLAnywhere para .NET 3.5 |16+ |16+ |Tabelas/modos de exibição |[Link de download](http://go.microsoft.com/fwlink/?linkid=324846) |

>[!NOTE]
>Arquivos do Excel com extensão .xlsx não exigem instalação separada do provedor.

>[!NOTE]
>Os provedores da Oracle também exigem software cliente da Oracle (versão 8.1.7+).

>[!NOTE]
>Para conexão a MySQL necessário utilizar versão anterior a 8.0.17. Recomendada a versão 6.10.9 disponível no link https://dev.mysql.com/downloads/connector/net/6.10.html.
> 
> 

