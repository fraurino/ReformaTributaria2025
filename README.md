# 📊 Classificação Tributária - Reforma Tributária Brasil
---

**Sistema de gerenciamento de dados tributários conforme a Reforma Tributária Brasileira (Lei Complementar nº 214/2025)**

<img width="1920" height="1040" alt="image" src="https://github.com/user-attachments/assets/cc32c198-f6bf-40c0-adfb-5be857cf99bc" />

## Funcionalidades

✅ Carregamento de arquivo JSON com dados de classificação tributária  
✅ Busca de CST pela classificação tributária  
✅ Busca de classificações pelo CST  
✅ Preenchimento automático de StringGrid com filtros  
✅ Suporte completo a caracteres acentuados (UTF-8)  
✅ 35+ campos tributários por classificação  

## Como Usar

### 1. Carregar Arquivo JSON
```delphi
var
  Gerenciador: TGerenciadorClassificacaoTributaria;
begin
  Gerenciador := TGerenciadorClassificacaoTributaria.Create('caminho/classificacao_tributaria.json');
  try
    Gerenciador.Carregar;
    ShowMessage('Total de registros: ' + IntToStr(Gerenciador.ObterTotal));
  finally
    Gerenciador.Free;
  end;
end;
```

### 2. Buscar CST pela Classificação
```delphi
var
  CST: string;
begin
  CST := Gerenciador.BuscarCSTporClasificacao('000001');
  ShowMessage('CST: ' + CST); // Resultado: 000
end;
```

### 3. Buscar Classificações pelo CST
```delphi
var
  ListaClassificacoes: TList<string>;
  i: Integer;
begin
  ListaClassificacoes := Gerenciador.BuscarClassificacaoPorCST('200');
  try
    for i := 0 to ListaClassificacoes.Count - 1 do
      ShowMessage(ListaClassificacoes[i]);
  finally
    ListaClassificacoes.Free;
  end;
end;
```

### 4. Preencher StringGrid
```delphi
// Todos os registros
PreencherStringGridCompleto(StringGrid1, Gerenciador);

// Filtrado por CST
PreencherStringGridPorCST(StringGrid1, Gerenciador, '200');

// Filtrado por classificação
PreencherStringGridPorClassificacao(StringGrid1, Gerenciador, '000001');
```

## Campos Disponíveis

- Código da Situação Tributária (CST)
- Descrição do CST
- Código da Classificação Tributária
- Descrição da Classificação
- Percentuais de redução (IBS/CBS)
- Flags: Diferimento, Monofásica, NFe, NFCe, CTe, etc.
- Tipo de alíquota
- Número do anexo
- URL da legislação

## Fonte de Dados

**Classificação Tributária**: https://dfe-portal.svrs.rs.gov.br/CFF/ClassificacaoTributaria

## Requisitos

- Delphi XE ou superior
- File com JSON da classificação tributária (UTF-8)

## Units Necessárias
```delphi
uses
  System.SysUtils,
  System.Generics.Collections,
  System.IOUtils,
  System.StrUtils,
  System.JSON;
```

**Lei Complementar nº 214/2025** - Reforma Tributária Brasileira (IBS e CBS)

---
---
📢 Conteúdo abaixo é uma campanha publicitária e não faz parte deste repositório.

# 💼 Classe para Reforma Tributária — Classe Pascal (Delphi/Lazarus)
---
## 🧠 O que é a **Classe RT**

A **Classe Reforma Tributária (TFuncoesAdicionaisRT)** foi desenvolvida para simplificar a adequação de sistemas ERP, PDV e emissores fiscais à nova estrutura da **CBS** e **IBS**, com base nas normas oficiais da Reforma Tributária.

✔️ **Compatível com Delphi e Lazarus (99%)**  
✔️ **Códigos e cálculos auxiliares na emissão com a reforma tributária**  
✔️ **Automação das regras tributárias CBS/IBS**  
✔️ **Integração modular e rápida com sistemas existentes**

![License: Proprietary](https://img.shields.io/badge/license-Proprietary-red.svg)
![Status](https://img.shields.io/badge/status-Active-success.svg)
![Delphi](https://img.shields.io/badge/Delphi-Compatible-blue.svg)
![Lazarus](https://img.shields.io/badge/Lazarus-Compatible-orange.svg)

## 🌐 Acesse o site oficial 👉 [rt.aurino.com.br](https://rt.aurino.com.br/?utm_source=github&utm_medium=readme&utm_campaign=reforma_tributaria)



