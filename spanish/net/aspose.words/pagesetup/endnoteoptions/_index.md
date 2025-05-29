---
title: PageSetup.EndnoteOptions
linktitle: EndnoteOptions
articleTitle: EndnoteOptions
second_title: Aspose.Words para .NET
description: Descubra la propiedad PageSetup EndnoteOptions para personalizar fácilmente la numeración y el posicionamiento de las notas finales para mejorar el formato y la claridad del documento.
type: docs
weight: 120
url: /es/net/aspose.words/pagesetup/endnoteoptions/
---
## PageSetup.EndnoteOptions property

Proporciona opciones que controlan la numeración y el posicionamiento de las notas finales en esta sección.

```csharp
public EndnoteOptions EndnoteOptions { get; }
```

## Ejemplos

Muestra cómo configurar las opciones que afectan las notas al pie y las notas finales de una sección.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote reference text.");

// Configurar todas las notas al pie en la primera sección para reiniciar la numeración desde 1
// en cada nueva página y se muestran directamente debajo del texto en cada página.
FootnoteOptions footnoteOptions = doc.Sections[0].PageSetup.FootnoteOptions;
footnoteOptions.Position = FootnotePosition.BeneathText;
footnoteOptions.RestartRule = FootnoteNumberingRule.RestartPage;
footnoteOptions.StartNumber = 1;

builder.Write(" Hello again.");
builder.InsertFootnote(FootnoteType.Footnote, "Endnote reference text.");

// Configure todas las notas finales en la primera sección para mantener un recuento continuo a lo largo de la sección,
// comenzando desde 1. Además, configúrelos todos para que aparezcan recopilados al final del documento.
EndnoteOptions endnoteOptions = doc.Sections[0].PageSetup.EndnoteOptions;
endnoteOptions.Position = EndnotePosition.EndOfDocument;
endnoteOptions.RestartRule = FootnoteNumberingRule.Continuous;
endnoteOptions.StartNumber = 1;

doc.Save(ArtifactsDir + "PageSetup.FootnoteOptions.docx");
```

### Ver también

* class [EndnoteOptions](../../../aspose.words.notes/endnoteoptions/)
* class [PageSetup](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
