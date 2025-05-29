---
title: ImportFormatOptions.SmartStyleBehavior
linktitle: SmartStyleBehavior
articleTitle: SmartStyleBehavior
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die SmartStyleBehavior-Eigenschaft von ImportFormatOptions den Import von Stilen mit gleichen Namen in Dokumenten optimiert. Passen Sie Ihren Importprozess mühelos an!
type: docs
weight: 80
url: /de/net/aspose.words/importformatoptions/smartstylebehavior/
---
## ImportFormatOptions.SmartStyleBehavior property

Ruft einen booleschen Wert ab oder legt ihn fest, der angibt, wie Stile importiert werden, wenn sie in Quell- und Zieldokumenten gleiche Namen haben. Der Standardwert ist`FALSCH` .

```csharp
public bool SmartStyleBehavior { get; set; }
```

## Bemerkungen

Wenn diese Option**ermöglicht** , wird der Quellstil in ein direktes Attribut innerhalb eines -Zieldokuments erweitert, wennKeepSourceFormatting Der Importmodus wird verwendet.

Wenn diese Option**deaktiviert**, der Quellstil wird nur erweitert, wenn er nummeriert ist. Vorhandene -Zielattribute werden nicht überschrieben, einschließlich Listen.

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

* class [ImportFormatOptions](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
