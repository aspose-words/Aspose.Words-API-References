---
title: "Aspose::Words::Style::get_NextParagraphStyleName‑Methode"
linktitle: "get_NextParagraphStyleName"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Style::get_NextParagraphStyleName‑Methode. Liest/legt den Namen des Stils fest, der automatisch auf einen neuen Absatz angewendet wird, der nach einem mit dem angegebenen Stil formatierten Absatz in C++ eingefügt wird."
type: docs
weight: 15000
url: /de/cpp/aspose.words/style/get_nextparagraphstylename/
---
## Style::get_NextParagraphStyleName method


Liest/Setzt den Namen des Stils, der automatisch auf einen neuen Absatz angewendet wird, der nach einem mit dem angegebenen Stil formatierten Absatz eingefügt wird.

```cpp
System::String Aspose::Words::Style::get_NextParagraphStyleName()
```


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

## Siehe auch

* Class [Style](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
