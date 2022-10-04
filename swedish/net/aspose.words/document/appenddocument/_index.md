---
title: AppendDocument
second_title: Aspose.Words för .NET API Referens
description: Lägger till det angivna dokumentet i slutet av detta dokument.
type: docs
weight: 510
url: /sv/net/aspose.words/document/appenddocument/
---
## AppendDocument(Document, ImportFormatMode) {#appenddocument}

Lägger till det angivna dokumentet i slutet av detta dokument.

```csharp
public void AppendDocument(Document srcDoc, ImportFormatMode importFormatMode)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| srcDoc | Document | Dokumentet som ska bifogas. |
| importFormatMode | ImportFormatMode | Anger hur stilformatering som krockar sammanfogas. |

### Exempel

Visar hur man lägger till ett dokument i slutet av ett annat dokument.

```csharp
Document srcDoc = new Document();
srcDoc.FirstSection.Body.AppendParagraph("Source document text. ");

Document dstDoc = new Document();
dstDoc.FirstSection.Body.AppendParagraph("Destination document text. ");

// Lägg till källdokumentet till måldokumentet samtidigt som du behåller dess formatering,
// spara sedan källdokumentet till det lokala filsystemet.
dstDoc.AppendDocument(srcDoc, ImportFormatMode.KeepSourceFormatting);
dstDoc.Save(ArtifactsDir + "Document.AppendDocument.docx");
```

Visar hur du lägger till alla dokument i en mapp i slutet av ett malldokument.

```csharp
Document dstDoc = new Document();

DocumentBuilder builder = new DocumentBuilder(dstDoc);
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Writeln("Template Document");
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Normal;
builder.Writeln("Some content here");

// Lägg till alla okrypterade dokument med tillägget .doc
// från vår lokala filsystemkatalog till basdokumentet.
List<string> docFiles = Directory.GetFiles(MyDir, "*.doc").Where(item => item.EndsWith(".doc")).ToList();
foreach (string fileName in docFiles)
{
    FileFormatInfo info = FileFormatUtil.DetectFileFormat(fileName);
    if (info.IsEncrypted)
        continue;

    Document srcDoc = new Document(fileName);
    dstDoc.AppendDocument(srcDoc, ImportFormatMode.UseDestinationStyles);
}

dstDoc.Save(ArtifactsDir + "Document.AppendAllDocumentsInFolder.doc");
```

### Se även

* enum [ImportFormatMode](../../importformatmode/)
* class [Document](../)
* namnutrymme [Aspose.Words](../../document/)
* hopsättning [Aspose.Words](../../../)

---

## AppendDocument(Document, ImportFormatMode, ImportFormatOptions) {#appenddocument_1}

Lägger till det angivna dokumentet i slutet av detta dokument.

```csharp
public void AppendDocument(Document srcDoc, ImportFormatMode importFormatMode, 
    ImportFormatOptions importFormatOptions)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| srcDoc | Document | Dokumentet som ska bifogas. |
| importFormatMode | ImportFormatMode | Anger hur stilformatering som krockar sammanfogas. |
| importFormatOptions | ImportFormatOptions | Tillåter att ange alternativ som påverkar formateringen av ett resultatdokument. |

### Exempel

Visar hur man hanterar liststilkrockar samtidigt som man lägger till en klon av ett dokument till sig själv.

```csharp
Document srcDoc = new Document(MyDir + "List item.docx");
Document dstDoc = new Document(MyDir + "List item.docx");

// Om det finns en konflikt mellan liststilar, använd listformatet för källdokumentet.
// Ställ in egenskapen "KeepSourceNumbering" till "false" för att inte importera några listnummer till måldokumentet.
// Ställ in "KeepSourceNumbering"-egenskapen till "true" importera all clashing
// liststilsnumrering med samma utseende som den hade i källdokumentet.
DocumentBuilder builder = new DocumentBuilder(dstDoc);
builder.MoveToDocumentEnd();
builder.InsertBreak(BreakType.SectionBreakNewPage);

ImportFormatOptions options = new ImportFormatOptions();
options.KeepSourceNumbering = keepSourceNumbering;
builder.InsertDocument(srcDoc, ImportFormatMode.KeepSourceFormatting, options);

dstDoc.UpdateListLabels();
```

Visar hur man hanterar liststilkrockar när ett dokument infogas.

```csharp
Document dstDoc = new Document();
DocumentBuilder builder = new DocumentBuilder(dstDoc);
builder.InsertBreak(BreakType.ParagraphBreak);

dstDoc.Lists.Add(ListTemplate.NumberDefault);
Aspose.Words.Lists.List list = dstDoc.Lists[0];

builder.ListFormat.List = list;

for (int i = 1; i <= 15; i++)
    builder.Write($"List Item {i}\n");

Document attachDoc = (Document)dstDoc.Clone(true);

// Om det finns en konflikt mellan liststilar, använd listformatet för källdokumentet.
// Ställ in egenskapen "KeepSourceNumbering" till "false" för att inte importera några listnummer till måldokumentet.
// Ställ in "KeepSourceNumbering"-egenskapen till "true" importera all clashing
// liststilsnumrering med samma utseende som den hade i källdokumentet.
ImportFormatOptions importOptions = new ImportFormatOptions();
importOptions.KeepSourceNumbering = keepSourceNumbering;

builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.InsertDocument(attachDoc, ImportFormatMode.KeepSourceFormatting, importOptions);

dstDoc.Save(ArtifactsDir + "DocumentBuilder.InsertDocumentAndResolveStyles.docx");
```

Visar hur du hanterar liststilkrockar medan du lägger till ett dokument.

```csharp
// Ladda ett dokument med text i en anpassad stil och klona den.
Document srcDoc = new Document(MyDir + "Custom list numbering.docx");
Document dstDoc = srcDoc.Clone();

// Vi har nu två dokument, var och en med en identisk stil som heter "CustomStyle".
// Ändra textfärgen för en av stilarna för att skilja den från den andra.
dstDoc.Styles["CustomStyle"].Font.Color = Color.DarkRed;

// Om det finns en konflikt mellan liststilar, använd listformatet för källdokumentet.
// Ställ in egenskapen "KeepSourceNumbering" till "false" för att inte importera några listnummer till måldokumentet.
// Ställ in "KeepSourceNumbering"-egenskapen till "true" importera all clashing
// liststilsnumrering med samma utseende som den hade i källdokumentet.
ImportFormatOptions options = new ImportFormatOptions();
options.KeepSourceNumbering = keepSourceNumbering;

// Att slå samman två dokument som har olika stilar som delar samma namn orsakar en stilkrock.
// Vi kan ange ett importformatläge när vi lägger till dokument för att lösa denna konflikt.
dstDoc.AppendDocument(srcDoc, ImportFormatMode.KeepDifferentStyles, options);
dstDoc.UpdateListLabels();

dstDoc.Save(ArtifactsDir + "DocumentBuilder.AppendDocumentAndResolveStyles.docx");
```

### Se även

* enum [ImportFormatMode](../../importformatmode/)
* class [ImportFormatOptions](../../importformatoptions/)
* class [Document](../)
* namnutrymme [Aspose.Words](../../document/)
* hopsättning [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
