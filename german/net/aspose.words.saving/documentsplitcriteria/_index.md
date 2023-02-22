---
title: Enum DocumentSplitCriteria
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Saving.DocumentSplitCriteria opsomming. Gibt an wie das Dokument beim Speichern in Teile aufgeteilt wirdHtml oderEpub format.
type: docs
weight: 4700
url: /de/net/aspose.words.saving/documentsplitcriteria/
---
## DocumentSplitCriteria enumeration

Gibt an, wie das Dokument beim Speichern in Teile aufgeteilt wirdHtml oderEpub format.

```csharp
[Flags]
public enum DocumentSplitCriteria
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| None | `0` | Das Dokument wird nicht geteilt. |
| PageBreak | `1` | Das Dokument wird an expliziten Seitenumbrüchen in Teile geteilt. Ein Seitenumbruch kann durch a angegeben werden[`PageBreak`](../../aspose.words/controlchar/pagebreak/) Zeichen, ein Abschnittsumbruch, der den Beginn eines neuen Abschnitts auf einer neuen Seite angibt, oder ein Absatz, der einen hat[`PageBreakBefore`](../../aspose.words/paragraphformat/pagebreakbefore/) Eigenschaft gesetzt auf`Stimmt` . |
| ColumnBreak | `2` | Das Dokument wird an Spaltenumbrüchen in Teile geteilt. Ein Spaltenumbruch kann durch a angegeben werden[`ColumnBreak`](../../aspose.words/controlchar/columnbreak/) Zeichen oder ein Abschnittsumbruch, der den Beginn eines neuen Abschnitts in einer neuen Spalte angibt. |
| SectionBreak | `4` | Das Dokument wird bei einem beliebigen Abschnittsumbruch in Teile geteilt. |
| HeadingParagraph | `8` | Das Dokument wird an einem mit einer Überschriftenvorlage formatierten Absatz in Teile geteilt **Überschrift 1** , **Überschrift 2** usw. Verwendung zusammen mit[`DocumentSplitHeadingLevel`](../htmlsaveoptions/documentsplitheadinglevel/) um die Überschriftenebenen (von 1 bis zur angegebenen Ebene) anzugeben, bei denen geteilt werden soll. |

### Bemerkungen

`DocumentSplitCriteria`ist ein Satz von Flags, die kombiniert werden können. Beispielsweise können Sie das Dokument document an Seitenumbrüchen und Überschriftabsätzen im selben Exportvorgang aufteilen.

Unterschiedliche Kriterien können sich teilweise überschneiden. Zum Beispiel, **Überschrift 1** Stil wird häufig angegeben [`PageBreakBefore`](../../aspose.words/paragraphformat/pagebreakbefore/) Eigentum, so dass es unter zwei Kriterien fällt:PageBreak und HeadingParagraph. Einige Abschnittsumbrüche können Seitenumbrüche usw. verursachen. In typischen Fällen ist die Angabe nur eines Flags die praktischste Option.

### Beispiele

Zeigt, wie Sie beim Speichern eines Dokuments im .epub-Format eine bestimmte Codierung verwenden.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Verwenden Sie ein SaveOptions-Objekt, um die Kodierung für ein zu speicherndes Dokument anzugeben.
HtmlSaveOptions saveOptions = new HtmlSaveOptions();
saveOptions.SaveFormat = SaveFormat.Epub;
saveOptions.Encoding = Encoding.UTF8;

// Standardmäßig hat ein ausgegebenes .epub-Dokument seinen gesamten Inhalt in einem HTML-Teil.
// Ein Split-Kriterium ermöglicht es uns, das Dokument in mehrere HTML-Teile zu segmentieren.
// Wir werden die Kriterien festlegen, um das Dokument in Überschriftenabsätze aufzuteilen.
// Dies ist nützlich für Leser, die keine HTML-Dateien lesen können, die größer als eine bestimmte Größe sind.
saveOptions.DocumentSplitCriteria = DocumentSplitCriteria.HeadingParagraph;

// Geben Sie an, dass wir Dokumenteigenschaften exportieren möchten.
saveOptions.ExportDocumentProperties = true;

doc.Save(ArtifactsDir + "HtmlSaveOptions.Doc2EpubSaveOptions.epub", saveOptions);
```

### Siehe auch

* namensraum [Aspose.Words.Saving](../../aspose.words.saving/)
* Montage [Aspose.Words](../../)


