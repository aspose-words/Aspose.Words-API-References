---
title: Document.AppendDocument
linktitle: AppendDocument
articleTitle: AppendDocument
second_title: Aspose.Words für .NET
description: Mit unserer Methode „Dokument anhängen“ können Sie mühelos Dokumente anhängen. Verbessern Sie Ihren Workflow durch die nahtlose Integration von Inhalten in Ihre vorhandenen Dateien.
type: docs
weight: 570
url: /de/net/aspose.words/document/appenddocument/
---
## AppendDocument(*[Document](../), [ImportFormatMode](../../importformatmode/)*) {#appenddocument}

Fügt das angegebene Dokument an das Ende dieses Dokuments an.

```csharp
public void AppendDocument(Document srcDoc, ImportFormatMode importFormatMode)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| srcDoc | Document | Das anzuhängende Dokument. |
| importFormatMode | ImportFormatMode | Gibt an, wie kollidierende Stilformatierungen zusammengeführt werden. |

## Beispiele

Zeigt, wie ein Dokument an das Ende eines anderen Dokuments angehängt wird.

```csharp
Document srcDoc = new Document();
srcDoc.FirstSection.Body.AppendParagraph("Source document text. ");

Document dstDoc = new Document();
dstDoc.FirstSection.Body.AppendParagraph("Destination document text. ");

// Das Quelldokument unter Beibehaltung der Formatierung an das Zieldokument anhängen,
// Speichern Sie dann das Quelldokument im lokalen Dateisystem.
dstDoc.AppendDocument(srcDoc, ImportFormatMode.KeepSourceFormatting);
dstDoc.Save(ArtifactsDir + "Document.AppendDocument.docx");
```

Zeigt, wie alle Dokumente in einem Ordner an das Ende eines Vorlagendokuments angehängt werden.

```csharp
Document dstDoc = new Document();

DocumentBuilder builder = new DocumentBuilder(dstDoc);
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Writeln("Template Document");
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Normal;
builder.Writeln("Some content here");
// Alle unverschlüsselten Dokumente mit der Erweiterung .doc anhängen
// von unserem lokalen Dateisystemverzeichnis zum Basisdokument.
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

### Siehe auch

* enum [ImportFormatMode](../../importformatmode/)
* class [Document](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)

---

## AppendDocument(*[Document](../), [ImportFormatMode](../../importformatmode/), [ImportFormatOptions](../../importformatoptions/)*) {#appenddocument_1}

Fügt das angegebene Dokument an das Ende dieses Dokuments an.

```csharp
public void AppendDocument(Document srcDoc, ImportFormatMode importFormatMode, 
    ImportFormatOptions importFormatOptions)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| srcDoc | Document | Das anzuhängende Dokument. |
| importFormatMode | ImportFormatMode | Gibt an, wie kollidierende Stilformatierungen zusammengeführt werden. |
| importFormatOptions | ImportFormatOptions | Ermöglicht die Angabe von Optionen, die die Formatierung eines Ergebnisdokuments beeinflussen. |

## Beispiele

Zeigt, wie Konflikte im Listenstil beim Anhängen eines Klons eines Dokuments an sich selbst behoben werden.

```csharp
Document srcDoc = new Document(MyDir + "List item.docx");
Document dstDoc = new Document(MyDir + "List item.docx");

// Wenn es zu einem Konflikt zwischen Listenstilen kommt, wenden Sie das Listenformat des Quelldokuments an.
// Setzen Sie die Eigenschaft „KeepSourceNumbering“ auf „false“, um keine Listennummern in das Zieldokument zu importieren.
// Setzen Sie die Eigenschaft "KeepSourceNumbering" auf "true" und importieren Sie alle
// Nummerierung im Listenstil mit demselben Erscheinungsbild wie im Quelldokument.
DocumentBuilder builder = new DocumentBuilder(dstDoc);
builder.MoveToDocumentEnd();
builder.InsertBreak(BreakType.SectionBreakNewPage);

ImportFormatOptions options = new ImportFormatOptions();
options.KeepSourceNumbering = keepSourceNumbering;
builder.InsertDocument(srcDoc, ImportFormatMode.KeepSourceFormatting, options);

dstDoc.UpdateListLabels();
```

Zeigt, wie Konflikte im Listenstil beim Einfügen eines Dokuments behoben werden.

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

// Wenn es zu einem Konflikt zwischen Listenstilen kommt, wenden Sie das Listenformat des Quelldokuments an.
// Setzen Sie die Eigenschaft „KeepSourceNumbering“ auf „false“, um keine Listennummern in das Zieldokument zu importieren.
// Setzen Sie die Eigenschaft "KeepSourceNumbering" auf "true" und importieren Sie alle
// Nummerierung im Listenstil mit demselben Erscheinungsbild wie im Quelldokument.
ImportFormatOptions importOptions = new ImportFormatOptions();
importOptions.KeepSourceNumbering = keepSourceNumbering;

builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.InsertDocument(attachDoc, ImportFormatMode.KeepSourceFormatting, importOptions);

dstDoc.Save(ArtifactsDir + "DocumentBuilder.InsertDocumentAndResolveStyles.docx");
```

Zeigt, wie Konflikte im Listenstil beim Anhängen eines Dokuments behoben werden.

```csharp
// Laden Sie ein Dokument mit Text in einem benutzerdefinierten Stil und klonen Sie es.
Document srcDoc = new Document(MyDir + "Custom list numbering.docx");
Document dstDoc = srcDoc.Clone();

// Wir haben jetzt zwei Dokumente, jedes mit einem identischen Stil namens „CustomStyle“.
// Ändern Sie die Textfarbe für einen der Stile, um ihn vom anderen abzuheben.
dstDoc.Styles["CustomStyle"].Font.Color = Color.DarkRed;

// Wenn es zu einem Konflikt zwischen Listenstilen kommt, wenden Sie das Listenformat des Quelldokuments an.
// Setzen Sie die Eigenschaft „KeepSourceNumbering“ auf „false“, um keine Listennummern in das Zieldokument zu importieren.
// Setzen Sie die Eigenschaft "KeepSourceNumbering" auf "true" und importieren Sie alle
// Nummerierung im Listenstil mit demselben Erscheinungsbild wie im Quelldokument.
ImportFormatOptions options = new ImportFormatOptions();
options.KeepSourceNumbering = keepSourceNumbering;

// Das Zusammenführen zweier Dokumente mit unterschiedlichen Stilen und demselben Namen führt zu einem Stilkonflikt.
// Wir können beim Anhängen von Dokumenten einen Importformatmodus angeben, um diesen Konflikt zu beheben.
dstDoc.AppendDocument(srcDoc, ImportFormatMode.KeepDifferentStyles, options);
dstDoc.UpdateListLabels();

dstDoc.Save(ArtifactsDir + "DocumentBuilder.AppendDocumentAndResolveStyles.docx");
```

### Siehe auch

* enum [ImportFormatMode](../../importformatmode/)
* class [ImportFormatOptions](../../importformatoptions/)
* class [Document](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
