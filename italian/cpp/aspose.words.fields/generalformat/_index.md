---
title: "Aspose::Words::Fields::GeneralFormat enum"
linktitle: "GeneralFormat"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fields::GeneralFormat enum. Specifica un formato generale applicato a un risultato numerico, testuale o di qualsiasi campo. Un campo può avere una combinazione di formati generali in C++."
type: docs
weight: 132000
url: /it/cpp/aspose.words.fields/generalformat/
---
## GeneralFormat enum


Specifica un formato generale applicato a un risultato numerico, di testo o di qualsiasi campo. Un campo può avere una combinazione di formati generali.

```cpp
enum class GeneralFormat
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| None | 0 | Utilizzato per specificare un formato generale mancante. |
| Aiueo | 1 | Formattazione numerica. Formatta un risultato numerico usando caratteri hiragana nell'ordine tradizionale a-i-u-e-o. |
| UppercaseAlphabetic | 2 | Formattazione numerica. Formatta un risultato numerico come una o più occorrenze di un carattere alfabetico latino maiuscolo. |
| LowercaseAlphabetic | 3 | Formattazione numerica. Formatta un risultato numerico come una o più occorrenze di un carattere alfabetico latino minuscolo. |
| Arabo | 4 | Formattazione numerica. Formatta un risultato numerico usando numeri cardinali arabi. |
| ArabicAbjad | 5 | Formattazione numerica. Formatta un risultato numerico usando numeri Abjad ascendente. |
| ArabicAlpha | 6 | Formattazione numerica. Formatta un risultato numerico usando caratteri dell'alfabeto arabo. |
| ArabicDash | 7 | Formattazione numerica. Formatta un risultato numerico usando numeri cardinali arabi, con un prefisso di "- " e un suffisso di " -". |
| BahtText | 8 | Formattazione numerica. Formatta un risultato numerico nel sistema di numerazione tailandese. |
| CardText | 9 | Formattazione numerica. Testo cardinale (One, Two, Three, ...). |
| ChineseNum1 | 10 | Formattazione numerica. Formatta un risultato numerico utilizzando numeri in ordine crescente dal sistema di conteggio appropriato. |
| ChineseNum2 | 11 | Formattazione numerica. Formatta un risultato numerico utilizzando numeri sequenziali dal formato legale appropriato. |
| ChineseNum3 | 12 | Formattazione numerica. Formatta un risultato numerico utilizzando numeri sequenziali dal sistema di conteggio delle migliaia appropriato. |
| Chosung | 13 | Formattazione numerica. Formatta un risultato numerico utilizzando numeri sequenziali dal formato coreano Chosung. |
| CircleNum | 14 | Formattazione numerica. Formatta un risultato numerico usando numerazione decimale racchiusa in un cerchio, utilizzando il glifo alfanumerico racchiuso per i numeri nell'intervallo 1–20. |
| DBChar | 15 | Formattazione numerica. Formatta un risultato numerico usando numerazione araba a doppio byte. |
| DBNum1 | 16 | Formattazione numerica. Formatta un risultato numerico usando ideogrammi digitali sequenziali, utilizzando il carattere appropriato. |
| DBNum2 | 17 | Formattazione numerica. Formatta un risultato numerico usando numeri sequenziali dal sistema di conteggio appropriato. |
| DBNum3 | 18 | Formattazione numerica. Formatta un risultato numerico usando numeri sequenziali dal sistema di conteggio legale appropriato. |
| DBNum4 | 19 | Formattazione numerica. Formatta un risultato numerico usando numeri sequenziali dal sistema di conteggio digitale appropriato. |
| DollarText | 20 | Formattazione numerica. Testo in dollari (One, Two, Three, ... + AND 55/100). |
| Ganada | 21 | Formattazione numerica. Formatta un risultato numerico usando numeri sequenziali dal formato coreano Ganada. |
| GB1 | 22 | Formattazione numerica. Formatta un risultato numerico usando numerazione decimale seguita da un punto, utilizzando il glifo alfanumerico racchiuso. |
| GB2 | 23 | Formattazione numerica. Formatta un risultato numerico usando numerazione decimale racchiusa tra parentesi, utilizzando il glifo alfanumerico racchiuso. |
| GB3 | 24 | Formattazione numerica. Formatta un risultato numerico usando numerazione decimale racchiusa in un cerchio, utilizzando il carattere glifo alfanumerico racchiuso. |
| GB4 | 25 | Formattazione numerica. Formatta un risultato numerico usando numerazione decimale racchiusa in un cerchio, utilizzando il carattere glifo alfanumerico racchiuso. |
| Hebrew1 | 26 | Formattazione numerica. Formatta un risultato numerico usando numeri ebraici. |
| Hebrew2 | 27 | Formattazione numerica. Formatta un risultato numerico usando l'alfabeto ebraico. |
| Esadecimale | 28 | Formattazione numerica. Formatta il risultato numerico usando cifre esadecimali maiuscole. |
| HindiArabic | 29 | Formattazione numerica. Formatta un risultato numerico usando numeri hindi. |
| HindiCardText | 30 | Formattazione numerica. Formatta un risultato numerico usando numeri sequenziali dal sistema di conteggio hindi. |
| HindiLetter1 | 31 | Formattazione numerica. Formatta un risultato numerico usando vocali hindi. |
| HindiLetter2 | 32 | Formattazione numerica. Formatta un risultato numerico usando consonanti hindi. |
| Iroha | 33 | Formattazione numerica. Formatta un risultato numerico usando l'iroha giapponese. |
| KanjiNum1 | 34 | Formattazione numerica. Formatta un risultato numerico usando uno stile giapponese con il sistema di conteggio appropriato. |
| KanjiNum2 | 35 | Formattazione numerica. Formatta un risultato numerico usando il sistema di conteggio appropriato. |
| KanjiNum3 | 36 | Formattazione numerica. Formatta un risultato numerico usando il sistema di conteggio appropriato. |
| Ordinal | 37 | Formattazione numerica. Ordinale (1°, 2°, 3°, ...). |
| OrdText | 38 | Formattazione numerica. Testo ordinali (Primo, Secondo, Terzo, ...). |
| UppercaseRoman | 39 | Formattazione numerica. Romani maiuscoli (I, II, III, ...). |
| LowercaseRoman | 40 | Formattazione numerica. Romani minuscoli (i, ii, iii, ...). |
| SBChar | 41 | Formattazione numerica. Formatta un risultato numerico usando numerazione araba a byte singolo. |
| ThaiArabic | 42 | Formattazione numerica. Formatta un risultato numerico usando numeri tailandesi. |
| ThaiCardText | 43 | Formattazione numerica. Formatta un risultato numerico usando numeri sequenziali dal sistema di conteggio tailandese. |
| ThaiLetter | 44 | Formattazione numerica. Formatta un risultato numerico usando lettere tailandesi. |
| VietCardText | 45 | Formattazione numerica. Formatta un risultato numerico usando numeri vietnamiti. |
| Zodiac1 | 46 | Formattazione numerica. Formatta un risultato numerico usando ideogrammi tradizionali numerici sequenziali. |
| Zodiac2 | 47 | Formattazione numerica. Formatta un risultato numerico usando ideogrammi zodiacali sequenziali. |
| Zodiac3 | 48 | Formattazione numerica. Formatta un risultato numerico usando ideogrammi zodiacali tradizionali sequenziali. |
| Maiuscole | 49 | Formattazione del testo. Converte in maiuscolo la prima lettera di ogni parola. |
| FirstCap | 50 | Formattazione del testo. Converte in maiuscolo la prima lettera della prima parola. |
| Minuscolo | 51 | Formattazione del testo. Tutte le lettere sono minuscole. |
| Maiuscolo | 52 | Formattazione del testo. Tutte le lettere sono maiuscole. |
| CharFormat | 53 | Formattazione del risultato di [Field](../field/). L'istruzione CHARFORMAT. |
| MergeFormat | 54 | Formattazione del risultato di [Field](../field/). L'istruzione MERGEFORMAT. |
| MergeFormatInet | 55 | Formattazione del risultato di [Field](../field/). L'istruzione MERGEFORMATINET. |


## Esempi



Mostra come formattare i risultati dei campi.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Usa un document builder per inserire un campo che visualizza un risultato senza alcun formato applicato.
System::SharedPtr<Aspose::Words::Fields::Field> field = builder->InsertField(u"= 2 + 3");

ASSERT_EQ(u"= 2 + 3", field->GetFieldCode());
ASSERT_EQ(u"5", field->get_Result());

// Possiamo applicare un formato al risultato di un campo usando le proprietà del campo.
// Di seguito sono riportati tre tipi di formati che possiamo applicare al risultato di un campo.
// 1 -  Formato numerico:
System::SharedPtr<Aspose::Words::Fields::FieldFormat> format = field->get_Format();
format->set_NumericFormat(u"$###.00");
field->Update();

ASSERT_EQ(u"= 2 + 3 \\# $###.00", field->GetFieldCode());
ASSERT_EQ(u"$  5.00", field->get_Result());

// 2 -  Formato data/ora:
field = builder->InsertField(u"DATE");
format = field->get_Format();
format->set_DateTimeFormat(u"dddd, MMMM dd, yyyy");
field->Update();

ASSERT_EQ(u"DATE \\@ \"dddd, MMMM dd, yyyy\"", field->GetFieldCode());
std::cout << System::String::Format(u"Today's date, in {0} format:\n\t{1}", format->get_DateTimeFormat(), field->get_Result()) << std::endl;

// 3 -  Formato generale:
field = builder->InsertField(u"= 25 + 33");
format = field->get_Format();
format->get_GeneralFormats()->Add(Aspose::Words::Fields::GeneralFormat::LowercaseRoman);
format->get_GeneralFormats()->Add(Aspose::Words::Fields::GeneralFormat::Upper);
field->Update();

int32_t index = 0;
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<Aspose::Words::Fields::GeneralFormat>> generalFormatEnumerator = format->get_GeneralFormats()->GetEnumerator();
    while (generalFormatEnumerator->MoveNext())
    {
        std::cout << System::String::Format(u"General format index {0}: {1}", index++, generalFormatEnumerator->get_Current()) << std::endl;
    }
}

ASSERT_EQ(u"= 25 + 33 \\* roman \\* Upper", field->GetFieldCode());
ASSERT_EQ(u"LVIII", field->get_Result());
ASSERT_EQ(2, format->get_GeneralFormats()->get_Count());
ASSERT_EQ(Aspose::Words::Fields::GeneralFormat::LowercaseRoman, format->get_GeneralFormats()->idx_get(0));

// Possiamo rimuovere i nostri formati per ripristinare il risultato del campo nella sua forma originale.
format->get_GeneralFormats()->Remove(Aspose::Words::Fields::GeneralFormat::LowercaseRoman);
format->get_GeneralFormats()->RemoveAt(0);
ASSERT_EQ(0, format->get_GeneralFormats()->get_Count());
field->Update();

ASSERT_EQ(u"= 25 + 33  ", field->GetFieldCode());
ASSERT_EQ(u"58", field->get_Result());
ASSERT_EQ(0, format->get_GeneralFormats()->get_Count());
```

## Vedi anche

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
