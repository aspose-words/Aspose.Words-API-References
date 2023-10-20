---
title: DocumentSplitCriteria Enum
linktitle: DocumentSplitCriteria
articleTitle: DocumentSplitCriteria
second_title: Aspose.Words für .NET
description: Aspose.Words.Saving.DocumentSplitCriteria opsomming. Gibt an wie das Dokument beim Speichern in Teile aufgeteilt wirdHtml  Epub oderAzw3 format in C#.
type: docs
weight: 4960
url: /de/net/aspose.words.saving/documentsplitcriteria/
---
## DocumentSplitCriteria enumeration

Gibt an, wie das Dokument beim Speichern in Teile aufgeteilt wirdHtml , Epub oderAzw3 format.

```csharp
[Flags]
public enum DocumentSplitCriteria
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| None | `0` | Das Dokument ist nicht geteilt. |
| PageBreak | `1` | Das Dokument wird bei expliziten Seitenumbrüchen in Teile geteilt. Ein Seitenumbruch kann durch a angegeben werden[`PageBreak`](../../aspose.words/controlchar/pagebreak/) Zeichen, ein Abschnittsumbruch, der den Beginn eines neuen Abschnitts auf einer neuen Seite angibt, oder ein Absatz, der sein eigenes hat[`PageBreakBefore`](../../aspose.words/paragraphformat/pagebreakbefore/) Eigenschaft festgelegt auf`WAHR` . |
| ColumnBreak | `2` | Das Dokument wird an Spaltenumbrüchen in Teile geteilt. Ein Spaltenumbruch kann durch a angegeben werden[`ColumnBreak`](../../aspose.words/controlchar/columnbreak/) Zeichen or ein Abschnittsumbruch, der den Beginn eines neuen Abschnitts in einer neuen Spalte angibt. |
| SectionBreak | `4` | Das Dokument wird bei einem Abschnittswechsel beliebiger Art in Teile geteilt. |
| HeadingParagraph | `8` | Das Dokument wird an einem Absatz, der mit einem Überschriftenstil formatiert wurde, in Teile geteilt**Überschrift 1** ,**Überschrift 2** usw. Zusammen mit verwenden[`DocumentSplitHeadingLevel`](../htmlsaveoptions/documentsplitheadinglevel/) um die Überschriftenebenen (von 1 bis zur angegebenen Ebene) anzugeben, auf denen geteilt werden soll. |

## Bemerkungen

`DocumentSplitCriteria`ist eine Reihe von Flags, die kombiniert werden können. Beispielsweise können Sie das Dokument an Seitenumbrüchen und Überschriftenabsätzen im selben Exportvorgang aufteilen.

Verschiedene Kriterien können sich teilweise überschneiden. Zum Beispiel,**Überschrift 1** Stil wird häufig mit angegeben[`PageBreakBefore`](../../aspose.words/paragraphformat/pagebreakbefore/) Eigentum und fällt daher unter zwei Kriterien:PageBreak und HeadingParagraph. Einige Abschnittsumbrüche können Seitenumbrüche usw. verursachen. In typischen Fällen ist die Angabe nur eines Flags die praktischste Option.

## Beispiele

Zeigt, wie beim Speichern eines Dokuments im .epub-Format eine bestimmte Kodierung verwendet wird.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Verwenden Sie ein SaveOptions-Objekt, um die Codierung für ein Dokument anzugeben, das wir speichern möchten.
HtmlSaveOptions saveOptions = new HtmlSaveOptions();
saveOptions.SaveFormat = SaveFormat.Epub;
saveOptions.Encoding = Encoding.UTF8;

// Standardmäßig enthält ein .epub-Ausgabedokument seinen gesamten Inhalt in einem HTML-Teil.
// Ein Split-Kriterium ermöglicht es uns, das Dokument in mehrere HTML-Teile zu segmentieren.
// Wir legen die Kriterien fest, um das Dokument in Überschriftenabsätze aufzuteilen.
// Dies ist nützlich für Leser, die keine HTML-Dateien lesen können, die größer als eine bestimmte Größe sind.
saveOptions.DocumentSplitCriteria = DocumentSplitCriteria.HeadingParagraph;

// Geben Sie an, dass wir Dokumenteigenschaften exportieren möchten.
saveOptions.ExportDocumentProperties = true;

doc.Save(ArtifactsDir + "HtmlSaveOptions.Doc2EpubSaveOptions.epub", saveOptions);
```

### Siehe auch

* namensraum [Aspose.Words.Saving](../../aspose.words.saving/)
* Montage [Aspose.Words](../../)
