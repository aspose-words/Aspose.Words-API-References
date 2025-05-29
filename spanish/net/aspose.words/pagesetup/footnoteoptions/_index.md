---
title: PageSetup.FootnoteOptions
linktitle: FootnoteOptions
articleTitle: FootnoteOptions
second_title: Aspose.Words para .NET
description: Descubra PageSetup FootnoteOptions para personalizar fácilmente la numeración y la posición de las notas al pie para lograr una mayor claridad y profesionalismo en el documento.
type: docs
weight: 150
url: /es/net/aspose.words/pagesetup/footnoteoptions/
---
## PageSetup.FootnoteOptions property

Proporciona opciones que controlan la numeración y el posicionamiento de las notas al pie en esta sección.

```csharp
public FootnoteOptions FootnoteOptions { get; }
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

* class [FootnoteOptions](../../../aspose.words.notes/footnoteoptions/)
* class [PageSetup](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
