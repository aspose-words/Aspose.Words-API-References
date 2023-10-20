---
title: ParagraphFormat.WidowControl
linktitle: WidowControl
articleTitle: WidowControl
second_title: Aspose.Words für .NET
description: ParagraphFormat WidowControl eigendom. True wenn die erste und letzte Zeile des Absatzes auf derselben Seite wie der Rest des Absatzes bleiben sollen in C#.
type: docs
weight: 400
url: /de/net/aspose.words/paragraphformat/widowcontrol/
---
## ParagraphFormat.WidowControl property

True, wenn die erste und letzte Zeile des Absatzes auf derselben Seite wie der Rest des Absatzes bleiben sollen.

```csharp
public bool WidowControl { get; set; }
```

## Beispiele

Zeigt, wie die Witwen-/Waisenkontrolle für einen Absatz aktiviert wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Wenn wir einen Text schreiben, der nicht auf eine Seite passt, kann eine Zeile auf die nächste Seite übergehen.
// Die einzelne Zeile, die auf der nächsten Seite landet, wird als „Orphan“ bezeichnet.
// und die vorherige Zeile, in der das Waisenkind abgebrochen hat, wird als „Witwe“ bezeichnet.
// Wir können Waisen und Witwen beheben, indem wir den Text anhand der Schriftgröße, des Abstands oder der Seitenränder neu anordnen.
// Wenn wir die Abmessungen unseres Dokuments beibehalten möchten, können wir dieses Flag auf „true“ setzen.
 // um Witwen auf die gleiche Seite wie ihre jeweiligen Waisen zu drängen.
// Wenn Sie dieses Flag auf „false“ belassen, bleiben Witwen-/Waisenpaare im Text.
// Für jeden Absatz ist diese Einstellung in Microsoft Word über Home -> zugänglich. Absatz -> Absatzeinstellungen
// (Schaltfläche in der unteren rechten Ecke der Registerkarte „Absatz“) -> „Witwen-/Waisenkontrolle“.
builder.ParagraphFormat.WidowControl = widowControl; 

// Text einfügen, der eine Waise und eine Witwe hervorbringt.
builder.Font.Size = 68;
builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc.Save(ArtifactsDir + "ParagraphFormat.WidowControl.docx");
```

### Siehe auch

* class [ParagraphFormat](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
