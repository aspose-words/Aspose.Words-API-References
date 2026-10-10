---
title: "Aspose::Words::ParagraphFormat::get_WidowControl Methode"
linktitle: "get_WidowControl"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::ParagraphFormat::get_WidowControl Methode. True, wenn die erste und letzte Zeile im Absatz auf derselben Seite wie der Rest des Absatzes in C++ bleiben sollen."
type: docs
weight: 41000
url: /de/cpp/aspose.words/paragraphformat/get_widowcontrol/
---
## ParagraphFormat::get_WidowControl method


True, wenn die erste und letzte Zeile im Absatz auf derselben Seite wie der Rest des Absatzes bleiben sollen.

```cpp
bool Aspose::Words::ParagraphFormat::get_WidowControl()
```


## Beispiele



Zeigt, wie man die Witwen-/Waisensteuerung für einen Absatz aktiviert.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Wenn wir den Text schreiben, der nicht auf eine Seite passt, kann eine Zeile auf die nächste Seite überlaufen.
// Die einzelne Zeile, die auf der nächsten Seite endet, wird "Orphan" genannt,
// und die vorherige Zeile, an der der orphan abbricht, wird "Widow" genannt.
// Wir können Waise und Witwen korrigieren, indem wir den Text durch Schriftgröße, Abstand oder Seitenränder neu anordnen.
// Wenn wir die Abmessungen unseres Dokuments beibehalten möchten, können wir dieses Flag auf "true" setzen
// um Witwen auf dieselbe Seite wie ihre jeweiligen Waise zu verschieben.
// Wenn dieses Flag auf "false" bleibt, bleiben Witwen/orphan-Paare im Text.
// Jeder Absatz hat diese Einstellung, die in Microsoft Word über Home -> Paragraph -> Paragraph Settings zugänglich ist
// (Schaltfläche in der unteren rechten Ecke des "Paragraph"-Tabs) -> "Widow/Orphan control".
builder->get_ParagraphFormat()->set_WidowControl(widowControl);

// Fügen Sie Text ein, der einen orphan und eine widow erzeugt.
builder->get_Font()->set_Size(68);
builder->Write(System::String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, ") + u"sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.WidowControl.docx");
```

## Siehe auch

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
