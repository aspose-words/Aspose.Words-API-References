---
title: TxtSaveOptions.PreserveTableLayout
linktitle: PreserveTableLayout
articleTitle: PreserveTableLayout
second_title: Aspose.Words für .NET
description: Entdecken Sie die Funktion „PreserveTableLayout“ von TxtSaveOptions, die sicherstellt, dass Ihre Tabellen beim Speichern als einfacher Text ihr Layout beibehalten. Verbessern Sie die Lesbarkeit Ihres Dokuments!
type: docs
weight: 50
url: /de/net/aspose.words.saving/txtsaveoptions/preservetablelayout/
---
## TxtSaveOptions.PreserveTableLayout property

Gibt an, ob das Programm versuchen soll, das Layout von Tabellen beim Speichern im Nur-Text-Format beizubehalten. Der Standardwert ist`FALSCH` .

```csharp
public bool PreserveTableLayout { get; set; }
```

## Beispiele

Zeigt, wie das Layout von Tabellen bei der Konvertierung in Klartext erhalten bleibt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, cell 1");
builder.InsertCell();
builder.Write("Row 1, cell 2");
builder.EndRow();
builder.InsertCell();
builder.Write("Row 2, cell 1");
builder.InsertCell();
builder.Write("Row 2, cell 2");
builder.EndTable();

// Erstellen Sie ein "TxtSaveOptions"-Objekt, das wir an die "Save"-Methode des Dokuments übergeben können
// um zu ändern, wie wir das Dokument im Klartext speichern.
TxtSaveOptions txtSaveOptions = new TxtSaveOptions();

// Setzen Sie die Eigenschaft „PreserveTableLayout“ auf „true“, um Leerzeichen auf den Inhalt anzuwenden
// des ausgegebenen Klartextdokuments, um möglichst viel vom Layout der Tabelle beizubehalten.
// Setzen Sie die Eigenschaft „PreserveTableLayout“ auf „false“, um alle Tabelleninhalte zu speichern
// als fortlaufender Textkörper, mit nur einer neuen Zeile für jede Reihe.
txtSaveOptions.PreserveTableLayout = preserveTableLayout;

doc.Save(ArtifactsDir + "TxtSaveOptions.PreserveTableLayout.txt", txtSaveOptions);

string docText = File.ReadAllText(ArtifactsDir + "TxtSaveOptions.PreserveTableLayout.txt");

if (preserveTableLayout)
    Assert.AreEqual("Row 1, cell 1                                            Row 1, cell 2\r\n" +
                    "Row 2, cell 1                                            Row 2, cell 2\r\n\r\n", docText);
else
    Assert.AreEqual("Row 1, cell 1\r" +
                    "Row 1, cell 2\r" +
                    "Row 2, cell 1\r" +
                    "Row 2, cell 2\r\r\n", docText);
```

### Siehe auch

* class [TxtSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
