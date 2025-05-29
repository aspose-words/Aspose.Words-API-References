---
title: TxtSaveOptions.SimplifyListLabels
linktitle: SimplifyListLabels
articleTitle: SimplifyListLabels
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die Funktion „SimplifyListLabels“ von TxtSaveOptions die Übersichtlichkeit verbessert, indem sie komplexe Listenbeschriftungen rationalisiert und so die Textdarstellung verbessert.
type: docs
weight: 70
url: /de/net/aspose.words.saving/txtsaveoptions/simplifylistlabels/
---
## TxtSaveOptions.SimplifyListLabels property

Gibt an, ob das Programm Listenbeschriftungen vereinfachen soll, falls komplexe Beschriftungsformatierungen nicht ausreichend durch einfachen Text dargestellt werden können.

Wenn eingestellt auf`WAHR` , nummerierte Listenbeschriftungen werden im einfachen numerischen Format und detaillierte Listenbeschriftungen als einfache ASCII-Zeichen geschrieben. Der Standardwert ist`FALSCH`.

```csharp
public bool SimplifyListLabels { get; set; }
```

## Beispiele

Zeigt, wie die Darstellung von Listen beim Speichern eines Dokuments im Klartext geändert wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Erstellen Sie eine Aufzählungsliste mit fünf Einrückungsebenen.
builder.ListFormat.ApplyBulletDefault();
builder.Writeln("Item 1");
builder.ListFormat.ListIndent();
builder.Writeln("Item 2");
builder.ListFormat.ListIndent();
builder.Writeln("Item 3");
builder.ListFormat.ListIndent();
builder.Writeln("Item 4");
builder.ListFormat.ListIndent();
builder.Write("Item 5");

// Erstellen Sie ein "TxtSaveOptions"-Objekt, das wir an die "Save"-Methode des Dokuments übergeben können
// um zu ändern, wie wir das Dokument im Klartext speichern.
TxtSaveOptions txtSaveOptions = new TxtSaveOptions();

// Setzen Sie die Eigenschaft "SimplifyListLabels" auf "true", um eine Liste zu konvertieren
// Symbole in einfachere ASCII-Zeichen wie „*“, „o“, „+“, „>“ usw.
// Setzen Sie die Eigenschaft „SimplifyListLabels“ auf „false“, um möglichst viele ursprüngliche Listensymbole beizubehalten.
txtSaveOptions.SimplifyListLabels = simplifyListLabels;

doc.Save(ArtifactsDir + "TxtSaveOptions.SimplifyListLabels.txt", txtSaveOptions);

string docText = File.ReadAllText(ArtifactsDir + "TxtSaveOptions.SimplifyListLabels.txt");

string newLine = Environment.NewLine;

if (simplifyListLabels)
    Assert.AreEqual($"* Item 1{newLine}" +
                    $"  > Item 2{newLine}" +
                    $"    + Item 3{newLine}" +
                    $"      - Item 4{newLine}" +
                    $"        o Item 5{newLine}", docText);
else
    Assert.AreEqual($"· Item 1{newLine}" +
                    $"o Item 2{newLine}" +
                    $"§ Item 3{newLine}" +
                    $"· Item 4{newLine}" +
                    $"o Item 5{newLine}", docText);
```

### Siehe auch

* class [TxtSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
