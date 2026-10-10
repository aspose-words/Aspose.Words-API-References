---
title: "Aspose::Words::Lists::ListLabel::get_LabelString Methode"
linktitle: "get_LabelString"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Lists::ListLabel::get_LabelString Methode. Gibt eine Zeichenkettenrepräsentation des ListLabels in C++ zurück."
type: docs
weight: 3000
url: /de/cpp/aspose.words.lists/listlabel/get_labelstring/
---
## ListLabel::get_LabelString method


Ermittelt eine Zeichenkettenrepräsentation des ListLabels.

```cpp
System::String Aspose::Words::Lists::ListLabel::get_LabelString()
```


## Beispiele



Zeigt, wie man die ListLabels aller Absätze extrahiert, die Listeneinträge sind.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");
doc->UpdateListLabels();

System::SharedPtr<Aspose::Words::NodeCollection> paras = doc->GetChildNodes(Aspose::Words::NodeType::Paragraph, true);

// Finden Sie heraus, ob wir die Absatzliste haben. In unserem Dokument verwendet unsere Liste einfache arabische Zahlen,
// die bei drei beginnen und bei sechs enden.
for (auto&& paragraph : paras->LINQ_OfType<System::SharedPtr<Aspose::Words::Paragraph> >()->LINQ_Where(static_cast<System::Func<System::SharedPtr<Aspose::Words::Paragraph>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Paragraph> p)>>([](System::SharedPtr<Aspose::Words::Paragraph> p) -> bool
{
    return p->get_ListFormat()->get_IsListItem();
})))->LINQ_ToList())
{
    std::cout << System::String::Format(u"List item paragraph #{0}", paras->IndexOf(paragraph)) << std::endl;

    // Dies ist der Text, den wir erhalten, wenn wir diesen Knoten in das Textformat ausgeben.
    // Diese Textausgabe lässt ListLabels weg. Entfernen Sie alle Absatzformatierungszeichen.
    System::String paragraphText = paragraph->ToString(Aspose::Words::SaveFormat::Text).Trim();
    std::cout << System::String::Format(u"\tExported Text: {0}", paragraphText) << std::endl;

    System::SharedPtr<Aspose::Words::Lists::ListLabel> label = paragraph->get_ListLabel();

    // Dies ermittelt die Position des Absatzes in der aktuellen Ebene der Liste. Wenn wir eine Liste mit mehreren Ebenen haben,
    // wird uns sagen, welche Position er auf dieser Ebene hat.
    std::cout << System::String::Format(u"\tNumerical Id: {0}", label->get_LabelValue()) << std::endl;

    // Kombinieren Sie sie, um das ListLabel zusammen mit dem Text in der Ausgabe einzuschließen.
    std::cout << System::String::Format(u"\tList label combined with text: {0} {1}", label->get_LabelString(), paragraphText) << std::endl;
}
```

## Siehe auch

* Class [ListLabel](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
