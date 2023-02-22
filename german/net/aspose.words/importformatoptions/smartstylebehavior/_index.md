---
title: ImportFormatOptions.SmartStyleBehavior
second_title: Aspose.Words für .NET-API-Referenz
description: ImportFormatOptions eigendom. Ruft einen booleschen Wert ab oder legt ihn fest der angibt wie Stile importiert werden  wenn sie in Quell und Zieldokumenten denselben Namen haben. Der Standardwert istFALSCH .
type: docs
weight: 70
url: /de/net/aspose.words/importformatoptions/smartstylebehavior/
---
## ImportFormatOptions.SmartStyleBehavior property

Ruft einen booleschen Wert ab oder legt ihn fest, der angibt, wie Stile importiert werden , wenn sie in Quell- und Zieldokumenten denselben Namen haben. Der Standardwert ist`FALSCH` .

```csharp
public bool SmartStyleBehavior { get; set; }
```

### Bemerkungen

Wenn diese Option ist **aktiviert** , wird der Quellstil in direkte Attribute innerhalb des Zieldokuments a erweitert, wennKeepSourceFormatting Importmodus verwendet wird.

Wenn diese Option ist **deaktiviert**, wird der Quellstil nur erweitert, wenn er nummeriert ist. Vorhandene -Zielattribute werden nicht überschrieben, einschließlich Listen.

### Beispiele

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

// Klonen Sie das Dokument und bearbeiten Sie den "MyStyle"-Stil des Klons, sodass er eine andere Farbe als das Original hat.
// Wenn wir den Klon in das Originaldokument einfügen, verursachen die beiden Stile mit demselben Namen einen Konflikt.
Document srcDoc = dstDoc.Clone();
srcDoc.Styles["MyStyle"].Font.Color = Color.Red;

// Wenn wir SmartStyleBehavior aktivieren und den Importformatmodus KeepSourceFormatting verwenden,
// Aspose.Words löst Stilkonflikte durch Konvertieren von Quelldokumentstilen.
// mit denselben Namen wie Zielstile in direkte Absatzattribute.
ImportFormatOptions options = new ImportFormatOptions();
options.SmartStyleBehavior = true;

builder.InsertDocument(srcDoc, ImportFormatMode.KeepSourceFormatting, options);

dstDoc.Save(ArtifactsDir + "DocumentBuilder.SmartStyleBehavior.docx");
```

### Siehe auch

* class [ImportFormatOptions](../)
* namensraum [Aspose.Words](../../importformatoptions/)
* Montage [Aspose.Words](../../../)


