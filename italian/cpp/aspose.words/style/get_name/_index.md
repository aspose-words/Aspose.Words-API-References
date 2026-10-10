---
title: "Metodo Aspose::Words::Style::get_Name"
linktitle: "get_Name"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Style::get_Name. Ottiene o imposta il nome dello stile in C++."
type: docs
weight: 14000
url: /it/cpp/aspose.words/style/get_name/
---
## Style::get_Name method


Ottiene o imposta il nome dello stile.

```cpp
System::String Aspose::Words::Style::get_Name() const
```

## Note


Non può essere una stringa vuota.

Se esiste già uno stile con quel nome nella collezione, questo stile lo sovrascriverà. Tutti i nodi interessati faranno riferimento al nuovo stile.

## Esempi



Mostra come accedere alla raccolta di stili di un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

ASSERT_EQ(4, doc->get_Styles()->get_Count());

// Elenca e visualizza tutti gli stili che un documento creato con Aspose.Words contiene per impostazione predefinita.
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


Mostra come clonare lo stile di un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Il metodo AddCopy crea una copia dello stile specificato e
// genera automaticamente un nuovo nome per lo stile, ad esempio "Heading 1_0".
System::SharedPtr<Aspose::Words::Style> newStyle = doc->get_Styles()->AddCopy(doc->get_Styles()->idx_get(u"Heading 1"));

// Utilizza la proprietà "Name" dello stile per modificare il nome identificativo dello stile.
newStyle->set_Name(u"My Heading 1");

// Il nostro documento ora ha due stili dall'aspetto identico con nomi diversi.
// Modificare le impostazioni di uno dei due stili non influisce sull'altro.
newStyle->get_Font()->set_Color(System::Drawing::Color::get_Red());

ASSERT_EQ(u"My Heading 1", newStyle->get_Name());
ASSERT_EQ(u"Heading 1", doc->get_Styles()->idx_get(u"Heading 1")->get_Name());

ASSERT_EQ(doc->get_Styles()->idx_get(u"Heading 1")->get_Type(), newStyle->get_Type());
ASSERT_EQ(doc->get_Styles()->idx_get(u"Heading 1")->get_Font()->get_Name(), newStyle->get_Font()->get_Name());
ASPOSE_ASSERT_EQ(doc->get_Styles()->idx_get(u"Heading 1")->get_Font()->get_Size(), newStyle->get_Font()->get_Size());
ASPOSE_ASSERT_NE(doc->get_Styles()->idx_get(u"Heading 1")->get_Font()->get_Color(), newStyle->get_Font()->get_Color());
```

## Vedi anche

* Class [Style](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
