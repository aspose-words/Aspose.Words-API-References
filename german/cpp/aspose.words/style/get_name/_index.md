---
title: "Aspose::Words::Style::get_Name Methode"
linktitle: "get_Name"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Style::get_Name Methode. Ruft den Namen des Stils ab oder legt ihn fest in C++."
type: docs
weight: 14000
url: /de/cpp/aspose.words/style/get_name/
---
## Style::get_Name method


Ruft den Namen des Stils ab bzw. legt ihn fest.

```cpp
System::String Aspose::Words::Style::get_Name() const
```

## Hinweise


Darf nicht leer sein.

Wenn bereits ein Stil mit diesem Namen in der Sammlung existiert, überschreibt dieser Stil ihn. Alle betroffenen Knoten verweisen auf den neuen Stil.

## Beispiele



Zeigt, wie auf die Formatvorlagensammlung eines Dokuments zugegriffen wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

ASSERT_EQ(4, doc->get_Styles()->get_Count());

// Auflisten und aufzählen aller Formatvorlagen, die ein mit Aspose.Words erstelltes Dokument standardmäßig enthält.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Style>>> stylesEnum = doc->get_Styles()->GetEnumerator();
    while (stylesEnum->MoveNext())
    {
        System::SharedPtr<Aspose::Words::Style> curStyle = stylesEnum->get_Current();
        std::cout << System::String::Format(u"Style name:\t\"{0}\", of type \"{1}\"", curStyle->get_Name(), curStyle->get_Type()) << std::endl;
        std::cout << System::String::Format(u"\tSubsequent style:\t{0}", curStyle->get_NextParagraphStyleName()) << std::endl;
        std::cout << System::String::Format(u"\tIs heading:\t\t\t{0}", curStyle->get_IsHeading()) << std::endl;
        std::cout << System::String::Format(u"\tIs QuickStyle:\t\t{0}", curStyle->get_IsQuickStyle()) << std::endl;

        ASPOSE_ASSERT_EQ(doc, curStyle->get_Document());
    }
}
```


Zeigt, wie man den Stil eines Dokuments klont.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Die AddCopy‑Methode erstellt eine Kopie des angegebenen Stils und
// generiert automatisch einen neuen Namen für den Stil, z. B. "Heading 1_0".
System::SharedPtr<Aspose::Words::Style> newStyle = doc->get_Styles()->AddCopy(doc->get_Styles()->idx_get(u"Heading 1"));

// Verwenden Sie die "Name"‑Eigenschaft des Stils, um den identifizierenden Namen des Stils zu ändern.
newStyle->set_Name(u"My Heading 1");

// Unser Dokument hat jetzt zwei identisch aussehende Stile mit unterschiedlichen Namen.
// Das Ändern der Einstellungen eines der Stile wirkt sich nicht auf den anderen aus.
newStyle->get_Font()->set_Color(System::Drawing::Color::get_Red());

ASSERT_EQ(u"My Heading 1", newStyle->get_Name());
ASSERT_EQ(u"Heading 1", doc->get_Styles()->idx_get(u"Heading 1")->get_Name());

ASSERT_EQ(doc->get_Styles()->idx_get(u"Heading 1")->get_Type(), newStyle->get_Type());
ASSERT_EQ(doc->get_Styles()->idx_get(u"Heading 1")->get_Font()->get_Name(), newStyle->get_Font()->get_Name());
ASPOSE_ASSERT_EQ(doc->get_Styles()->idx_get(u"Heading 1")->get_Font()->get_Size(), newStyle->get_Font()->get_Size());
ASPOSE_ASSERT_NE(doc->get_Styles()->idx_get(u"Heading 1")->get_Font()->get_Color(), newStyle->get_Font()->get_Color());
```

## Siehe auch

* Class [Style](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
