---
title: "Aspose::Words::NumSpacing enum"
linktitle: "NumSpacing"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::NumSpacing enum. Specifica i possibili valori in cui la spaziatura dei numeri può essere visualizzata in C++."
type: docs
weight: 103500
url: /it/cpp/aspose.words/numspacing/
---
## NumSpacing enum


Specifica i valori possibili in cui la spaziatura dei numeri può essere visualizzata.

```cpp
enum class NumSpacing
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Default | 0 | Specifica che i numeri sono visualizzati nella forma predefinita del font. |
| Proporzionale | 1 | Specifica che le forme dei numeri progettate come a spaziatura proporzionale sono visualizzate se supportate dal font. |
| Tabulare | 2 | Specifica che le forme dei numeri progettate come tabulari vengano visualizzate se supportate dal carattere. |


## Esempi



Mostra come impostare il tipo di spaziatura del numero.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Questo effetto è supportato solo nelle versioni più recenti di MS Word.
doc->get_CompatibilityOptions()->OptimizeFor(Aspose::Words::Settings::MsWordVersion::Word2019);

builder->Write(u"1 ");
builder->Write(u"This is an example");

System::SharedPtr<Aspose::Words::Run> run = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0);
if (run->get_Font()->get_NumberSpacing() == Aspose::Words::NumSpacing::Default)
{
    run->get_Font()->set_NumberSpacing(Aspose::Words::NumSpacing::Proportional);
}

doc->Save(get_ArtifactsDir() + u"Fonts.NumberSpacing.docx");
```

## Vedi anche

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
