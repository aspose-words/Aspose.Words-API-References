---
title: ImportFormatOptions Class
linktitle: ImportFormatOptions
articleTitle: ImportFormatOptions
second_title: Aspose.Words für .NET
description: Entdecken Sie Aspose.Words.ImportFormatOptions für anpassbare Dokumentformatierung. Verbessern Sie Ihre Ausgabe mit maßgeschneiderten Importeinstellungen für optimale Ergebnisse.
type: docs
weight: 3690
url: /de/net/aspose.words/importformatoptions/
---
## ImportFormatOptions class

Ermöglicht die Angabe verschiedener Importoptionen zum Formatieren der Ausgabe.

Um mehr zu erfahren, besuchen Sie die[Ladeoptionen festlegen](https://docs.aspose.com/words/net/specify-load-options/) Dokumentationsartikel.

```csharp
public class ImportFormatOptions
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [ImportFormatOptions](importformatoptions/)() | Default_Constructor |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [AdjustSentenceAndWordSpacing](../../aspose.words/importformatoptions/adjustsentenceandwordspacing/) { get; set; } | Ruft einen booleschen Wert ab oder legt ihn fest, der angibt, ob der Satz- und Wortabstand automatisch angepasst werden soll. Der Standardwert ist`FALSCH` . |
| [ForceCopyStyles](../../aspose.words/importformatoptions/forcecopystyles/) { get; set; } | Ruft einen booleschen Wert ab oder legt ihn fest, der angibt, ob widersprüchliche Stile kopiert werden sollen inKeepSourceFormatting mode. Der Standardwert ist`FALSCH` . |
| [IgnoreHeaderFooter](../../aspose.words/importformatoptions/ignoreheaderfooter/) { get; set; } | Ruft einen booleschen Wert ab oder legt ihn fest, der angibt, dass die Quellformatierung von Kopf-/Fußzeileninhalten ignoriert wird , wennKeepSourceFormatting Modus wird verwendet. Der Standardwert ist`WAHR` . |
| [IgnoreTextBoxes](../../aspose.words/importformatoptions/ignoretextboxes/) { get; set; } | Ruft einen booleschen Wert ab oder legt ihn fest, der angibt, dass die Quellformatierung des Inhalts von Textfeldern ignoriert wird , wennKeepSourceFormatting Modus wird verwendet. Der Standardwert ist`WAHR` . |
| [KeepSourceNumbering](../../aspose.words/importformatoptions/keepsourcenumbering/) { get; set; } | Ruft einen booleschen Wert ab oder legt ihn fest, der angibt, wie die Nummerierung importiert wird, wenn sie in Quell- und Zieldokumenten kollidiert. Der Standardwert ist`FALSCH` . |
| [MergePastedLists](../../aspose.words/importformatoptions/mergepastedlists/) { get; set; } | Ruft einen booleschen Wert ab oder legt ihn fest, der angibt, ob eingefügte Listen mit umgebenden Listen zusammengeführt werden. Der Standardwert ist`FALSCH` . |
| [SmartStyleBehavior](../../aspose.words/importformatoptions/smartstylebehavior/) { get; set; } | Ruft einen booleschen Wert ab oder legt ihn fest, der angibt, wie Stile importiert werden, wenn sie in Quell- und Zieldokumenten gleiche Namen haben. Der Standardwert ist`FALSCH` . |

## Beispiele

Zeigt, wie doppelte Stile beim Einfügen von Dokumenten aufgelöst werden.

```csharp
Document dstDoc = new Document();
DocumentBuilder builder = new DocumentBuilder(dstDoc);

Style myStyle = builder.Document.Styles.Add(StyleType.Paragraph, "MyStyle");
myStyle.Font.Size = 14;
myStyle.Font.Name = "Courier New";
myStyle.Font.Color = Color.Blue;

builder.ParagraphFormat.StyleName = myStyle.Name;
builder.Writeln("Hello world!");

// Klonen Sie das Dokument und bearbeiten Sie den „MyStyle“-Stil des Klons, sodass er eine andere Farbe als das Original hat.
// Wenn wir den Klon in das Originaldokument einfügen, kommt es aufgrund der beiden gleichnamigen Stile zu einem Konflikt.
Document srcDoc = dstDoc.Clone();
srcDoc.Styles["MyStyle"].Font.Color = Color.Red;

// Wenn wir SmartStyleBehavior aktivieren und den KeepSourceFormatting-Importformatmodus verwenden,
// Aspose.Words löst Stilkonflikte durch Konvertieren der Quelldokumentstile.
// mit denselben Namen wie Zielstile in direkte Absatzattribute.
ImportFormatOptions options = new ImportFormatOptions();
options.SmartStyleBehavior = true;

builder.InsertDocument(srcDoc, ImportFormatMode.KeepSourceFormatting, options);

dstDoc.Save(ArtifactsDir + "DocumentBuilder.SmartStyleBehavior.docx");
```

### Siehe auch

* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)
