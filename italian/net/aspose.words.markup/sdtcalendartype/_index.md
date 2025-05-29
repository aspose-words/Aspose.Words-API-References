---
title: SdtCalendarType Enum
linktitle: SdtCalendarType
articleTitle: SdtCalendarType
second_title: Aspose.Words per .NET
description: Esplora l'enum Aspose.Words.Markup.SdtCalendarType per arricchire i tuoi documenti Office Open XML con opzioni di calendario versatili per una migliore efficienza del flusso di lavoro.
type: docs
weight: 4690
url: /it/net/aspose.words.markup/sdtcalendartype/
---
## SdtCalendarType enumeration

Specifica i possibili tipi di calendari che possono essere utilizzati per specificare[`CalendarType`](../structureddocumenttag/calendartype/) in un documento Office Open XML.

```csharp
public enum SdtCalendarType
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Default | `0` | Utilizzato come valore predefinito in OOXML. Uguale aGregorian . |
| Gregorian | `0` | Specifica che deve essere utilizzato il calendario gregoriano, come definito in ISO 8601. Questo calendario deve essere localizzato nella lingua appropriata. |
| GregorianArabic | `1` | Specifica che deve essere utilizzato il calendario gregoriano, come definito in ISO 8601. I valori per questo calendario devono essere presentati in arabo. |
| GregorianMeFrench | `2` | Specifica che deve essere utilizzato il calendario gregoriano, come definito in ISO 8601. I valori per questo calendario devono essere presentati in francese mediorientale. |
| GregorianUs | `3` | Specifica che deve essere utilizzato il calendario gregoriano, come definito in ISO 8601. I valori per questo calendario devono essere presentati in inglese. |
| GregorianXlitEnglish | `4` | Specifica che deve essere utilizzato il calendario gregoriano, come definito in ISO 8601. I valori per questo calendario devono essere la rappresentazione delle stringhe inglesi nei corrispondenti caratteri arabi (la traslitterazione araba dell'inglese per il calendario gregoriano). |
| GregorianXlitFrench | `5` | Specifica che deve essere utilizzato il calendario gregoriano, come definito in ISO 8601. I valori per questo calendario devono essere la rappresentazione delle stringhe francesi nei corrispondenti caratteri arabi (la traslitterazione araba del francese per il calendario gregoriano). |
| Hebrew | `6` | Specifica che deve essere utilizzato il calendario lunare ebraico, come descritto dalla formula di Gauss per la Pasqua [CITAZIONE] e la Riformulazione completa della legge orale (Mishneh Torah). |
| Hijri | `7` | Specifica che verrà utilizzato il calendario lunare Hijri, come descritto dal Regno dell'Arabia Saudita, Ministero degli Affari Islamici, delle Dotazioni, della Da'wah e della Guida. |
| Japan | `8` | Specifica che deve essere utilizzato il calendario dell'era dell'imperatore giapponese, come descritto dallo standard industriale giapponese JIS X 0301. |
| Korea | `9` | Specifica che deve essere utilizzato il calendario coreano dell'era Tangun, come descritto dalla legge coreana n. 4. |
| None | `10` | Specifica che non deve essere utilizzato alcun calendario. |
| Saka | `11` | Specifica che deve essere utilizzato il calendario dell'era Saka, come descritto dal Comitato per la riforma del calendario dell'India, come parte dell'Effemeridi indiane e dell'Almanacco nautico. |
| Taiwan | `12` | Specifica che deve essere utilizzato il calendario taiwanese, come definito dallo standard nazionale cinese CNS 7648. |
| Thai | `13` | Specifica che deve essere utilizzato il calendario thailandese, come definito dal decreto reale di Sua Maestà il Re Vajiravudh (Rama VI) nella Gazzetta Reale BE 2456 (1913 d.C.) e dal decreto del Primo Ministro Phibunsongkhram (1941 d.C.) per iniziare l'anno il 1° gennaio gregoriano e per mappare l'anno zero all'anno gregoriano 543 a.C. |

## Esempi

Mostra come richiedere all'utente di immettere una data con un tag di documento strutturato.

```csharp
Document doc = new Document();

// Inserire un tag di documento strutturato che richieda all'utente di immettere una data.
// In Microsoft Word, questo elemento è noto come "controllo contenuto selettore data".
// Quando clicchiamo sulla freccia all'estremità destra di questo tag in Microsoft Word,
// vedremo apparire un pop-up sotto forma di calendario cliccabile.
// Possiamo usare quel popup per selezionare una data che verrà visualizzata dal tag.
StructuredDocumentTag sdtDate = new StructuredDocumentTag(doc, SdtType.Date, MarkupLevel.Inline);

// Visualizza la data in base alle impostazioni locali dell'Arabia Saudita.
sdtDate.DateDisplayLocale = CultureInfo.GetCultureInfo("ar-SA").LCID;

// Imposta il formato con cui visualizzare la data.
sdtDate.DateDisplayFormat = "dd MMMM, yyyy";
sdtDate.DateStorageFormat = SdtDateStorageFormat.DateTime;

// Visualizza la data secondo il calendario Hijri.
sdtDate.CalendarType = SdtCalendarType.Hijri;

// Prima che l'utente scelga una data in Microsoft Word, il tag visualizzerà il testo "Fai clic qui per immettere una data".
// In base al calendario del tag, imposta la proprietà "FullDate" per far sì che il tag visualizzi una data predefinita.
sdtDate.FullDate = new DateTime(1440, 10, 20);

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertNode(sdtDate);

doc.Save(ArtifactsDir + "StructuredDocumentTag.Date.docx");
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Markup](../../aspose.words.markup/)
* assemblea [Aspose.Words](../../)
