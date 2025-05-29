---
title: ParagraphFormat.WidowControl
linktitle: WidowControl
articleTitle: WidowControl
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die ParagraphFormat WidowControl-Eigenschaft sicherstellt, dass die erste und die letzte Zeile Ihres Textes für eine bessere Lesbarkeit auf derselben Seite bleiben.
type: docs
weight: 410
url: /de/net/aspose.words/paragraphformat/widowcontrol/
---
## ParagraphFormat.WidowControl property

Wahr, wenn die erste und die letzte Zeile des Absatzes auf derselben Seite bleiben sollen wie der Rest des Absatzes.

```csharp
public bool WidowControl { get; set; }
```

## Beispiele

Zeigt, wie die Hurenkinder-/Schneiderkontrolle für einen Absatz aktiviert wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Wenn wir Text schreiben, der nicht auf eine Seite passt, kann es sein, dass eine Zeile auf die nächste Seite überläuft.
// Die einzelne Zeile, die auf der nächsten Seite landet, wird als „Waise“ bezeichnet.
// und die vorherige Zeile, in der das Waisenkind abgebrochen wurde, wird „Witwe“ genannt.
// Wir können Hurenkinder und Hurenkinder beheben, indem wir den Text hinsichtlich Schriftgröße, Abstand oder Seitenrändern neu anordnen.
// Wenn wir die Abmessungen unseres Dokuments beibehalten möchten, können wir dieses Flag auf „true“ setzen.
// um Hurenkinder auf die gleiche Seite zu schieben wie ihre jeweiligen Waisen.
// Wenn Sie dieses Flag auf „false“ belassen, verbleiben Hurenkinderpaare im Text.
// Jeder Absatz hat diese Einstellung in Microsoft Word über Start -> Absatz -> Absatzeinstellungen zugänglich
// (Schaltfläche in der unteren rechten Ecke der Registerkarte „Absatz“) -> „Schurkenkontrolle“.
builder.ParagraphFormat.WidowControl = widowControl; 

// Text einfügen, der ein Waisenkind und eine Witwe erzeugt.
builder.Font.Size = 68;
builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc.Save(ArtifactsDir + "ParagraphFormat.WidowControl.docx");
```

### Siehe auch

* class [ParagraphFormat](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
