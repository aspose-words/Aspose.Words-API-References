---
title: ListLevel.IsLegal
linktitle: IsLegal
articleTitle: IsLegal
second_title: Aspose.Words für .NET
description: Entdecken Sie ListLevel IsLegal. Steuern Sie übernommene Nummernformate mühelos. Wählen Sie Arabisch für einen modernen Look oder behalten Sie die ursprünglichen Formate für einen klassischen Touch bei.
type: docs
weight: 50
url: /de/net/aspose.words.lists/listlevel/islegal/
---
## ListLevel.IsLegal property

Wahr, wenn die Ebene alle übernommenen Zahlen in arabische Zahlen umwandelt, falsch, wenn ihr Zahlenstil beibehalten wird.

```csharp
public bool IsLegal { get; set; }
```

## Beispiele

Zeigt erweiterte Möglichkeiten zum Anpassen von Listenbeschriftungen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Eine Liste ermöglicht es uns, Absatzsätze mit Präfixsymbolen und Einzügen zu organisieren und zu dekorieren.
    // Wir können verschachtelte Listen erstellen, indem wir die Einrückungsebene erhöhen.
    // Wir können eine Liste beginnen und beenden, indem wir die Eigenschaft „ListFormat“ eines Dokument-Generators verwenden.
// Jeder Absatz, den wir zwischen dem Anfang und dem Ende einer Liste hinzufügen, wird zu einem Element in der Liste.
List list = doc.Lists.Add(ListTemplate.NumberDefault);

// Beschriftungen der Ebene 1 werden entsprechend dem Absatzstil „Überschrift 1“ formatiert und haben ein Präfix.
// Diese sehen wie „Anhang A“, „Anhang B“ … aus.
list.ListLevels[0].NumberFormat = "Appendix \x0000";
list.ListLevels[0].NumberStyle = NumberStyle.UppercaseLetter;
list.ListLevels[0].LinkedStyle = doc.Styles["Heading 1"];

// Beschriftungen der Ebene 2 zeigen die aktuellen Nummern der ersten und zweiten Listenebene an und haben führende Nullen.
// Wenn die erste Listenebene bei 1 liegt, dann sehen die Listenbeschriftungen daraus wie folgt aus: „Abschnitt (1.01)“, „Abschnitt (1.02)“ …
list.ListLevels[1].NumberFormat = "Section (\x0000.\x0001)";
list.ListLevels[1].NumberStyle = NumberStyle.LeadingZero;

// Beachten Sie, dass auf höherer Ebene die Nummerierung in Großbuchstaben erfolgt.
// Wir können die Eigenschaft „IsLegal“ so einstellen, dass für die höheren Listenebenen arabische Zahlen verwendet werden.
list.ListLevels[1].IsLegal = true;
list.ListLevels[1].RestartAfterLevel = 0;

// Beschriftungen der Ebene 3 bestehen aus römischen Großbuchstaben mit einem Präfix und einem Suffix und werden bei jedem Listenelement der Ebene 1 neu gestartet.
// Diese Listenbeschriftungen sehen wie „-I-“, „-II-“ … aus.
list.ListLevels[2].NumberFormat = "-\x0002-";
list.ListLevels[2].NumberStyle = NumberStyle.UppercaseRoman;
list.ListLevels[2].RestartAfterLevel = 1;

// Beschriftungen aller Listenebenen fett machen.
foreach (ListLevel level in list.ListLevels)
    level.Font.Bold = true;

// Listenformatierung auf den aktuellen Absatz anwenden.
builder.ListFormat.List = list;

// Erstellen Sie Listenelemente, die alle drei unserer Listenebenen anzeigen.
for (int n = 0; n < 2; n++)
{
    for (int i = 0; i < 3; i++)
    {
        builder.ListFormat.ListLevelNumber = i;
        builder.Writeln("Level " + i);
    }
}

builder.ListFormat.RemoveNumbers();

doc.Save(ArtifactsDir + "Lists.CreateListRestartAfterHigher.docx");
```

### Siehe auch

* class [ListLevel](../)
* namensraum [Aspose.Words.Lists](../../../aspose.words.lists/)
* Montage [Aspose.Words](../../../)
