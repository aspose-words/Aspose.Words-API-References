---
title: "Aspose::Words::PageSetup::get_LineNumberDistanceFromText Methode"
linktitle: "get_LineNumberDistanceFromText"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::PageSetup::get_LineNumberDistanceFromText Methode. Gibt den Abstand zwischen dem rechten Rand der Zeilennummern und dem linken Rand des Dokuments zurück oder legt ihn fest in C++."
type: docs
weight: 24000
url: /de/cpp/aspose.words/pagesetup/get_linenumberdistancefromtext/
---
## PageSetup::get_LineNumberDistanceFromText method


Liest oder legt den Abstand zwischen dem rechten Rand der Zeilennummern und dem linken Rand des Dokuments fest.

```cpp
double Aspose::Words::PageSetup::get_LineNumberDistanceFromText()
```


## Beispiele



Zeigt, wie man die Zeilennummerierung für einen Abschnitt aktiviert.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Wir können das PageSetup-Objekt des Abschnitts verwenden, um die Nummern links von den Textzeilen des Abschnitts anzuzeigen.
// Dies ist das gleiche Verhalten wie bei einem List-Objekt,
// aber es deckt den gesamten Abschnitt ab und verändert den Text in keiner Weise.
// Unser Abschnitt wird die Nummerierung auf jeder neuen Seite bei 1 neu starten und die Nummer anzeigen,
// wenn sie ein Vielfaches von 3 ist, 50pt links von der Zeile.
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = builder->get_PageSetup();
pageSetup->set_LineStartingNumber(1);
pageSetup->set_LineNumberCountBy(3);
pageSetup->set_LineNumberRestartMode(Aspose::Words::LineNumberRestartMode::RestartPage);
pageSetup->set_LineNumberDistanceFromText(50.0);

for (int32_t i = 1; i <= 25; i++)
{
    builder->Writeln(System::String::Format(u"Line {0}.", i));
}

// Der Zeilenzähler wird jeden Absatz überspringen, bei dem das Flag "SuppressLineNumbers" auf "true" gesetzt ist.
// Dieser Absatz befindet sich in der 15. Zeile, die ein Vielfaches von 3 ist, und würde daher normalerweise eine Zeilennummer anzeigen.
// Der Zeilenzähler des Abschnitts wird diese Zeile ebenfalls ignorieren und die nächste Zeile als 15. behandeln,
// und die Zählung von diesem Punkt an fortsetzen.
doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(14)->get_ParagraphFormat()->set_SuppressLineNumbers(true);

doc->Save(get_ArtifactsDir() + u"PageSetup.LineNumbers.docx");
```

## Siehe auch

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
