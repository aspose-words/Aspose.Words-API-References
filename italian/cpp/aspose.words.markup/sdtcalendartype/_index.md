---
title: "Aspose::Words::Markup::SdtCalendarType enum"
linktitle: "SdtCalendarType"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Markup::SdtCalendarType enum. Specifica i possibili tipi di calendari che possono essere usati per specificare CalendarType in un documento Office Open XML in C++."
type: docs
weight: 19000
url: /it/cpp/aspose.words.markup/sdtcalendartype/
---
## SdtCalendarType enum


Specifica i possibili tipi di calendari che possono essere usati per specificare [CalendarType](../structureddocumenttag/get_calendartype/) in un documento Office Open XML.

```cpp
enum class SdtCalendarType
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Default | 0 | Usato come valore predefinito in OOXML. È uguale a [Gregorian](./). |
| Gregorian | n/a | Specifica che il calendario Gregoriano, così come definito nella ISO 8601, deve essere utilizzato. Questo calendario dovrebbe essere localizzato nella lingua appropriata. |
| GregorianArabic | n/a | Specifica che il calendario Gregoriano, così come definito nella ISO 8601, deve essere utilizzato. I valori per questo calendario dovrebbero essere presentati in arabo. |
| GregorianMeFrench | n/a | Specifica che il calendario Gregoriano, così come definito nella ISO 8601, deve essere utilizzato. I valori per questo calendario dovrebbero essere presentati in francese del Medio Oriente. |
| GregorianUs | n/a | Specifica che il calendario Gregoriano, così come definito nella ISO 8601, deve essere utilizzato. I valori per questo calendario dovrebbero essere presentati in inglese. |
| GregorianXlitEnglish | n/a | Specifica che il calendario Gregoriano, così come definito nella ISO 8601, deve essere utilizzato. I valori per questo calendario dovrebbero essere la rappresentazione delle stringhe in inglese nei corrispondenti caratteri arabi (la traslitterazione araba dell'inglese per il calendario Gregoriano). |
| GregorianXlitFrench | n/a | Specifica che il calendario Gregoriano, così come definito nella ISO 8601, deve essere utilizzato. I valori per questo calendario dovrebbero essere la rappresentazione delle stringhe in francese nei corrispondenti caratteri arabi (la traslitterazione araba del francese per il calendario Gregoriano). |
| Ebraico | n/a | Specifica che il calendario lunare ebraico, come descritto dalla formula di Gauss per la Pasqua [CITATION] e dal The Complete Restatement of Oral Law (Mishneh Torah), deve essere utilizzato. |
| Hijri | n/a | Specifica che il calendario lunare Hijri, come descritto dal Regno dell'Arabia Saudita, Ministero degli Affari Islamici, Endowment, Da‘wah e Guida, deve essere utilizzato. |
| Giappone | n/a | Specifica che il calendario dell'era imperiale giapponese, come descritto dallo Japanese Industrial Standard JIS X 0301, deve essere utilizzato. |
| Corea | n/a | Specifica che il calendario coreano dell'Era Tangun, come descritto dalla Legge Coreana n. 4, deve essere utilizzato. |
| None | n/a | Specifica che non deve essere utilizzato alcun calendario. |
| Saka | n/a | Specifica che il calendario dell'Era Saka, come descritto dal Comitato di Riforma del Calendario dell'India, parte dell'Ephemeris Indiano e dell'Almanacco Nautico, deve essere utilizzato. |
| Taiwan | n/a | Specifica che il calendario taiwanese, come definito dallo Standard Nazionale Cinese CNS 7648, deve essere utilizzato. |
| Thai | n/a | Specifica che il calendario tailandese, così definito dal Decreto Reale di Sua Maestà il Re Vajiravudh (Rama VI) nella Gazzetta Reale B. E. 2456 (1913 d.C.) e dal decreto del Primo Ministro Phibunsongkhram (1941 d.C.), deve iniziare l'anno il 1 gennaio del calendario gregoriano e mappare l'anno zero all'anno gregoriano 543 a.C., e deve essere utilizzato. |


## Esempi



Mostra come chiedere all'utente di inserire una data con un tag di documento strutturato.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Inserisci un tag di documento strutturato che richiede all'utente di inserire una data.
// In Microsoft Word, questo elemento è conosciuto come "Date picker content control".
// Quando facciamo clic sulla freccia all'estremità destra di questo tag in Microsoft Word,
// vedremo un pop up nella forma di un calendario cliccabile.
// Possiamo usare quel pop‑up per selezionare una data che il tag visualizzerà.
auto sdtDate = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::Date, Aspose::Words::Markup::MarkupLevel::Inline);

// Visualizza la data, secondo le impostazioni locali arabo‑saudite.
sdtDate->set_DateDisplayLocale(System::Globalization::CultureInfo::GetCultureInfo(u"ar-SA")->get_LCID());

// Imposta il formato con cui visualizzare la data.
sdtDate->set_DateDisplayFormat(u"dd MMMM, yyyy");
sdtDate->set_DateStorageFormat(Aspose::Words::Markup::SdtDateStorageFormat::DateTime);

// Visualizza la data secondo il calendario Hijri.
sdtDate->set_CalendarType(Aspose::Words::Markup::SdtCalendarType::Hijri);

// Prima che l'utente scelga una data in Microsoft Word, il tag visualizzerà il testo "Click here to enter a date.".
// Secondo il calendario del tag, imposta la proprietà "FullDate" per far visualizzare al tag una data predefinita.
sdtDate->set_FullDate(System::DateTime(1440, 10, 20));

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->InsertNode(sdtDate);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.Date.docx");
```

## Vedi anche

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
