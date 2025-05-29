---
title: Section.ClearHeadersFooters
linktitle: ClearHeadersFooters
articleTitle: ClearHeadersFooters
second_title: Aspose.Words für .NET
description: Mit der ClearHeadersFooters-Methode löschen Sie mühelos Abschnittskopf- und -fußzeilen. Optimieren Sie Ihr Dokumentlayout für ein elegantes Erscheinungsbild!
type: docs
weight: 120
url: /de/net/aspose.words/section/clearheadersfooters/
---
## ClearHeadersFooters() {#clearheadersfooters}

Löscht die Kopf- und Fußzeilen dieses Abschnitts.

```csharp
public void ClearHeadersFooters()
```

## Bemerkungen

Der Text aller Kopf- und Fußzeilen wird gelöscht, aber[`HeaderFooter`](../../headerfooter/) Objekte selbst werden nicht entfernt.

Dadurch werden Kopf- und Fußzeilen dieses Abschnitts mit Kopf- und Fußzeilen des vorherigen Abschnitts verknüpft.

## Beispiele

Zeigt, wie der Inhalt aller Kopf- und Fußzeilen in einem Abschnitt gelöscht wird.

```csharp
Document doc = new Document();

Assert.AreEqual(0, doc.FirstSection.HeadersFooters.Count);

DocumentBuilder builder = new DocumentBuilder(doc);

builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Writeln("This is the primary header.");
builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.Writeln("This is the primary footer.");

Assert.AreEqual(2, doc.FirstSection.HeadersFooters.Count);

Assert.AreEqual("This is the primary header.", doc.FirstSection.HeadersFooters[HeaderFooterType.HeaderPrimary].GetText().Trim());
Assert.AreEqual("This is the primary footer.", doc.FirstSection.HeadersFooters[HeaderFooterType.FooterPrimary].GetText().Trim());

// Leeren Sie alle Kopf- und Fußzeilen in diesem Abschnitt von ihrem gesamten Inhalt.
// Die Kopf- und Fußzeilen selbst sind noch vorhanden, haben aber nichts anzuzeigen.
doc.FirstSection.ClearHeadersFooters();

Assert.AreEqual(2, doc.FirstSection.HeadersFooters.Count);

Assert.AreEqual(string.Empty, doc.FirstSection.HeadersFooters[HeaderFooterType.HeaderPrimary].GetText().Trim());
Assert.AreEqual(string.Empty, doc.FirstSection.HeadersFooters[HeaderFooterType.FooterPrimary].GetText().Trim());
```

### Siehe auch

* class [Section](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)

---

## ClearHeadersFooters(*bool*) {#clearheadersfooters_1}

Löscht die Kopf- und Fußzeilen dieses Abschnitts.

```csharp
public void ClearHeadersFooters(bool preserveWatermarks)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| preserveWatermarks | Boolean | True, wenn die Wasserzeichen nicht entfernt werden sollen. |

## Bemerkungen

Der Text aller Kopf- und Fußzeilen wird gelöscht, aber[`HeaderFooter`](../../headerfooter/) Objekte selbst werden nicht entfernt.

Dadurch werden Kopf- und Fußzeilen dieses Abschnitts mit Kopf- und Fußzeilen des vorherigen Abschnitts verknüpft.

## Beispiele

Zeigt, wie der Inhalt von Kopf- und Fußzeile mit oder ohne Wasserzeichen gelöscht wird.

```csharp
Document doc = new Document(MyDir + "Header and footer types.docx");

// Fügen Sie ein Wasserzeichen im Klartext hinzu.
doc.Watermark.SetText("Aspose Watermark");

// Stellen Sie sicher, dass die Kopf- und Fußzeilen Inhalt haben.
HeaderFooterCollection headersFooters = doc.FirstSection.HeadersFooters;
Assert.AreEqual("First header", headersFooters[HeaderFooterType.HeaderFirst].GetText().Trim());
Assert.AreEqual("Second header", headersFooters[HeaderFooterType.HeaderEven].GetText().Trim());
Assert.AreEqual("Third header", headersFooters[HeaderFooterType.HeaderPrimary].GetText().Trim());
Assert.AreEqual("First footer", headersFooters[HeaderFooterType.FooterFirst].GetText().Trim());
Assert.AreEqual("Second footer", headersFooters[HeaderFooterType.FooterEven].GetText().Trim());
Assert.AreEqual("Third footer", headersFooters[HeaderFooterType.FooterPrimary].GetText().Trim());

// Entfernt alle Kopf- und Fußzeileninhalte außer Wasserzeichen.
doc.FirstSection.ClearHeadersFooters(true);

headersFooters = doc.FirstSection.HeadersFooters;
Assert.AreEqual("", headersFooters[HeaderFooterType.HeaderFirst].GetText().Trim());
Assert.AreEqual("", headersFooters[HeaderFooterType.HeaderEven].GetText().Trim());
Assert.AreEqual("", headersFooters[HeaderFooterType.HeaderPrimary].GetText().Trim());
Assert.AreEqual("", headersFooters[HeaderFooterType.FooterFirst].GetText().Trim());
Assert.AreEqual("", headersFooters[HeaderFooterType.FooterEven].GetText().Trim());
Assert.AreEqual("", headersFooters[HeaderFooterType.FooterPrimary].GetText().Trim());
Assert.AreEqual(WatermarkType.Text, doc.Watermark.Type);

// Entfernt alle Kopf- und Fußzeileninhalte einschließlich Wasserzeichen.
doc.FirstSection.ClearHeadersFooters(false);
Assert.AreEqual(WatermarkType.None, doc.Watermark.Type);
```

### Siehe auch

* class [Section](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
