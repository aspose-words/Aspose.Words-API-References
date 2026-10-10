---
title: "Aspose::Words::Node::ToString-Methode"
linktitle: "ToString"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Node::ToString-Methode. Exportiert den Inhalt des Knotens in einen String im angegebenen Format in C++."
type: docs
weight: 22000
url: /de/cpp/aspose.words/node/tostring/
---
## Node::ToString(Aspose::Words::SaveFormat) method


Exportiert den Inhalt des Knotens in eine Zeichenkette im angegebenen Format.

```cpp
System::String Aspose::Words::Node::ToString(Aspose::Words::SaveFormat saveFormat)
```


### ReturnValue

Der Inhalt des Knotens im angegebenen Format.

## Beispiele



Zeigt den Unterschied zwischen dem Aufruf der GetText- und ToString-Methoden an einem Knoten.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->InsertField(u"MERGEFIELD Field");

// GetText ruft den sichtbaren Text sowie Feldcodes und Sonderzeichen ab.
ASSERT_EQ(u"\u0013MERGEFIELD Field\u0014«Field»\u0015", doc->GetText().Trim());

// ToString liefert das Aussehen des Dokuments, wenn es in ein übergebenes Speicherformat gespeichert wird.
ASSERT_EQ(u"«Field»", doc->ToString(Aspose::Words::SaveFormat::Text).Trim());
```


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


Exportiert den Inhalt eines Knotens in einen String im HTML-Format.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

System::SharedPtr<Aspose::Words::Node> node = doc->get_LastSection()->get_Body()->get_LastParagraph();

// Wenn wir die ToString-Methode mit der html SaveFormat-Überladung aufrufen,
// konvertiert sie den Inhalt des Knotens in seine rohe HTML-Darstellung.
ASSERT_EQ(System::String(u"<p style=\"margin-top:0pt; margin-bottom:8pt; line-height:108%; font-size:12pt\">") + u"<span style=\"font-family:'Times New Roman'\">Hello World!</span>" + u"</p>", node->ToString(Aspose::Words::SaveFormat::Html));

// Wir können das Ergebnis dieser Konvertierung auch mit einem SaveOptions-Objekt ändern.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
saveOptions->set_ExportRelativeFontSize(true);

ASSERT_EQ(System::String(u"<p style=\"margin-top:0pt; margin-bottom:8pt; line-height:108%\">") + u"<span style=\"font-family:'Times New Roman'\">Hello World!</span>" + u"</p>", node->ToString(saveOptions));
```

## Siehe auch

* Enum [SaveFormat](../../saveformat/)
* Class [Node](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Node::ToString(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) method


Exportiert den Inhalt des Knotens in eine Zeichenkette unter Verwendung der angegebenen Speicheroptionen.

```cpp
System::String Aspose::Words::Node::ToString(const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Gibt die Optionen an, die steuern, wie der Knoten gespeichert wird. |

### ReturnValue

Der Inhalt des Knotens im angegebenen Format.

## Beispiele



Exportiert den Inhalt eines Knotens in einen String im HTML-Format.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

System::SharedPtr<Aspose::Words::Node> node = doc->get_LastSection()->get_Body()->get_LastParagraph();

// Wenn wir die ToString-Methode mit der html SaveFormat-Überladung aufrufen,
// konvertiert sie den Inhalt des Knotens in seine rohe HTML-Darstellung.
ASSERT_EQ(System::String(u"<p style=\"margin-top:0pt; margin-bottom:8pt; line-height:108%; font-size:12pt\">") + u"<span style=\"font-family:'Times New Roman'\">Hello World!</span>" + u"</p>", node->ToString(Aspose::Words::SaveFormat::Html));

// Wir können das Ergebnis dieser Konvertierung auch mit einem SaveOptions-Objekt ändern.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
saveOptions->set_ExportRelativeFontSize(true);

ASSERT_EQ(System::String(u"<p style=\"margin-top:0pt; margin-bottom:8pt; line-height:108%\">") + u"<span style=\"font-family:'Times New Roman'\">Hello World!</span>" + u"</p>", node->ToString(saveOptions));
```

## Siehe auch

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Node](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
