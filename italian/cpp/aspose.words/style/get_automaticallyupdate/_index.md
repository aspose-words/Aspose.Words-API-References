---
title: "Metodo Aspose::Words::Style::get_AutomaticallyUpdate"
linktitle: "get_AutomaticallyUpdate"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Style::get_AutomaticallyUpdate. Specifica se questo stile viene ridefinito automaticamente in base al valore appropriato in C++."
type: docs
weight: 4000
url: /it/cpp/aspose.words/style/get_automaticallyupdate/
---
## Style::get_AutomaticallyUpdate method


Specifica se questo stile è ridefinito automaticamente in base al valore appropriato.

```cpp
bool Aspose::Words::Style::get_AutomaticallyUpdate() const
```

## Note


Se il valore della proprietà è impostato su true, MS Word ridefinisce automaticamente lo stile corrente quando la formattazione del paragrafo appropriata è stata modificata.

La proprietà AutomaticallyUpdate è applicabile solo agli stili di paragrafo.

Il valore predefinito è **false**.

## Esempi



Mostra come creare e applicare uno stile personalizzato.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::Style> style = doc->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle");
style->get_Font()->set_Name(u"Times New Roman");
style->get_Font()->set_Size(16);
style->get_Font()->set_Color(System::Drawing::Color::get_Navy());
// Ridefinisci automaticamente lo stile.
style->set_AutomaticallyUpdate(true);

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Applica uno degli stili del documento al paragrafo che il document builder sta creando.
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"MyStyle"));
builder->Writeln(u"Hello world!");

System::SharedPtr<Aspose::Words::Style> firstParagraphStyle = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Style();

ASPOSE_ASSERT_EQ(style, firstParagraphStyle);

// Rimuovi il nostro stile personalizzato dalla raccolta di stili del documento.
doc->get_Styles()->idx_get(u"MyStyle")->Remove();

firstParagraphStyle = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Style();

// Qualsiasi testo che utilizzava uno stile rimosso ritorna alla formattazione predefinita.
ASSERT_FALSE(doc->get_Styles()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Style>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Style> s)>>([](System::SharedPtr<Aspose::Words::Style> s) -> bool
{
    return s->get_Name() == u"MyStyle";
}))));
ASSERT_EQ(u"Times New Roman", firstParagraphStyle->get_Font()->get_Name());
ASPOSE_ASSERT_EQ(12.0, firstParagraphStyle->get_Font()->get_Size());
ASSERT_EQ(System::Drawing::Color::Empty.ToArgb(), firstParagraphStyle->get_Font()->get_Color().ToArgb());
```

## Vedi anche

* Class [Style](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
