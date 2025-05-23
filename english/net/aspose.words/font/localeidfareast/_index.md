---
title: Font.LocaleIdFarEast
linktitle: LocaleIdFarEast
articleTitle: LocaleIdFarEast
second_title: Aspose.Words for .NET
description: Discover the Font LocaleIdFarEast property to easily manage locale identifiers for formatted Asian characters, enhancing your multilingual applications.
type: docs
weight: 220
url: /net/aspose.words/font/localeidfareast/
---
## Font.LocaleIdFarEast property

Gets or sets the locale identifier (language) of the formatted Asian characters.

```csharp
public int LocaleIdFarEast { get; set; }
```

## Remarks

For the list of locale identifiers see https://msdn.microsoft.com/en-us/library/cc233965.aspx

## Examples

Shows how to insert and format text in a Far East language.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Specify font settings that the document builder will apply to any text that it inserts.
builder.Font.Name = "Courier New";
builder.Font.LocaleId = new CultureInfo("en-US", false).LCID;

// Name "FarEast" equivalents for our font and locale.
// If the builder inserts Asian characters with this Font configuration, then each run that contains
// these characters will display them using the "FarEast" font/locale instead of the default.
// This could be useful when a western font does not have ideal representations for Asian characters.
builder.Font.NameFarEast = "SimSun";
builder.Font.LocaleIdFarEast = new CultureInfo("zh-CN", false).LCID;

// This text will be displayed in the default font/locale.
builder.Writeln("Hello world!");

// Since these are Asian characters, this run will apply our "FarEast" font/locale equivalents.
builder.Writeln("你好世界");

doc.Save(ArtifactsDir + "Font.FarEast.docx");
```

### See Also

* class [Font](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
