---
title: Font.NameFarEast
linktitle: NameFarEast
articleTitle: NameFarEast
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „Font NameFarEast“, um ostasiatische Schriftnamen für eine verbesserte Typografie in Ihren Projekten einfach anzupassen und festzulegen.
type: docs
weight: 260
url: /de/net/aspose.words/font/namefareast/
---
## Font.NameFarEast property

Gibt einen ostasiatischen Schriftnamen zurück oder legt ihn fest.

```csharp
public string NameFarEast { get; set; }
```

## Beispiele

Zeigt, wie man Text in einer fernöstlichen Sprache einfügt und formatiert.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Geben Sie die Schrifteinstellungen an, die der Dokumentgenerator auf jeden eingefügten Text anwendet.
builder.Font.Name = "Courier New";
builder.Font.LocaleId = new CultureInfo("en-US", false).LCID;

// Benennen Sie „FarEast“-Äquivalente für unsere Schriftart und unser Gebietsschema.
// Wenn der Builder asiatische Zeichen mit dieser Font-Konfiguration einfügt, dann wird jeder Lauf, der
// Diese Zeichen werden mit der Schriftart/Gebietsschema „FarEast“ anstelle der Standardeinstellung angezeigt.
// Dies kann nützlich sein, wenn eine westliche Schriftart keine ideale Darstellung für asiatische Zeichen bietet.
builder.Font.NameFarEast = "SimSun";
builder.Font.LocaleIdFarEast = new CultureInfo("zh-CN", false).LCID;

// Dieser Text wird in der Standardschriftart/-gebietsschema angezeigt.
builder.Writeln("Hello world!");

// Da es sich um asiatische Zeichen handelt, werden bei diesem Lauf unsere Schriftart-/Gebietsschema-Äquivalente „FarEast“ angewendet.
builder.Writeln("你好世界");

doc.Save(ArtifactsDir + "Font.FarEast.docx");
```

### Siehe auch

* property [Name](../name/)
* class [Font](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
