---
title: "EditingLanguage"
linktitle: "EditingLanguage"
second_title: "Aspose.Words لـ Java"
description: "يحدد لغة التحرير في Java."
type: docs
weight: 182
url: /ar/java/com.aspose.words/editinglanguage/
---

**Inheritance:**
java.lang.Object
```
public class EditingLanguage
```

يحدد لغة التحرير.

 **Examples:** 

يوضح كيفية تطبيق تفضيلات اللغة عند تحميل مستند.

```

 LoadOptions loadOptions = new LoadOptions();
 loadOptions.getLanguagePreferences().addEditingLanguage(EditingLanguage.JAPANESE);

 Document doc = new Document(getMyDir() + "No default editing language.docx", loadOptions);

 int localeIdFarEast = doc.getStyles().getDefaultFont().getLocaleIdFarEast();
 System.out.println(localeIdFarEast == EditingLanguage.JAPANESE
         ? "The document either has no any FarEast language set in defaults or it was set to Japanese originally."
         : "The document default FarEast language was set to another than Japanese language originally, so it is not overridden.");
 
```
## الحقول

| حقل | الوصف |
| --- | --- |
| [AFRIKAANS](#AFRIKAANS) | اللغة: Afrikaans |
| [ALBANIAN](#ALBANIAN) | اللغة: Albanian |
| [ALSATIAN](#ALSATIAN) | اللغة: Alsatian |
| [AMHARIC](#AMHARIC) | اللغة: Amharic |
| [ARABIC_ALGERIA](#ARABIC-ALGERIA) | اللغة: Arabic (Algeria) |
| [ARABIC_BAHRAIN](#ARABIC-BAHRAIN) | اللغة: Arabic (Bahrain) |
| [ARABIC_EGYPT](#ARABIC-EGYPT) | اللغة: Arabic (Egypt) |
| [ARABIC_IRAQ](#ARABIC-IRAQ) | اللغة: Arabic (Iraq) |
| [ARABIC_JORDAN](#ARABIC-JORDAN) | اللغة: العربية (الأردن) |
| [ARABIC_KUWAIT](#ARABIC-KUWAIT) | اللغة: العربية (الكويت) |
| [ARABIC_LEBANON](#ARABIC-LEBANON) | اللغة: العربية (لبنان) |
| [ARABIC_LIBYA](#ARABIC-LIBYA) | اللغة: العربية (ليبيا) |
| [ARABIC_MOROCCO](#ARABIC-MOROCCO) | اللغة: العربية (المغرب) |
| [ARABIC_OMAN](#ARABIC-OMAN) | اللغة: العربية (عمان) |
| [ARABIC_QATAR](#ARABIC-QATAR) | اللغة: العربية (قطر) |
| [ARABIC_SAUDI_ARABIA](#ARABIC-SAUDI-ARABIA) | اللغة: العربية (المملكة العربية السعودية) |
| [ARABIC_SYRIA](#ARABIC-SYRIA) | اللغة: العربية (سوريا) |
| [ARABIC_TUNISIA](#ARABIC-TUNISIA) | اللغة: العربية (تونس) |
| [ARABIC_UAE](#ARABIC-UAE) | اللغة: العربية (الإمارات العربية المتحدة) |
| [ARABIC_YEMEN](#ARABIC-YEMEN) | اللغة: العربية (اليمن) |
| [ARMENIAN](#ARMENIAN) | اللغة: الأرمنية |
| [ASSAMESE](#ASSAMESE) | اللغة: الأسامية |
| [AZERBAIJANI_CYRILLIC](#AZERBAIJANI-CYRILLIC) | اللغة: الأذربيجانية (سيريلية) |
| [AZERBAIJANI_LATIN](#AZERBAIJANI-LATIN) | اللغة: الأذربيجانية (لاتينية) |
| [BANGLA_BANGLADESH](#BANGLA-BANGLADESH) | اللغة: البنغالية (بنغلاديش) |
| [BANGLA_INDIA](#BANGLA-INDIA) | اللغة: البنغالية (الهند) |
| [BASHKIR](#BASHKIR) | اللغة: الباشكيرية |
| [BASQUE](#BASQUE) | اللغة: الباسكية |
| [BELARUSIAN](#BELARUSIAN) | اللغة: البيلاروسية |
| [BOSNIAN_CYRILLIC](#BOSNIAN-CYRILLIC) | اللغة: البوسنية (سيريلية) |
| [BOSNIAN_LATIN](#BOSNIAN-LATIN) | اللغة: البوسنية (لاتينية) |
| [BRETON](#BRETON) | اللغة: البريتونية |
| [BULGARIAN](#BULGARIAN) | اللغة: البلغارية |
| [BURMESE](#BURMESE) | اللغة: البورمية |
| [CATALAN](#CATALAN) | اللغة: الكتالونية |
| [CENTRAL_KURDISH_IRAQ](#CENTRAL-KURDISH-IRAQ) | اللغة: الكردية الوسطى (العراق) |
| [CHEROKEE](#CHEROKEE) | اللغة: الشيروكي |
| [CHINESE_HONG_KONG](#CHINESE-HONG-KONG) | اللغة: الصينية (هونغ كونغ) |
| [CHINESE_MACAO](#CHINESE-MACAO) | اللغة: الصينية (ماكاو) |
| [CHINESE_PRC](#CHINESE-PRC) | اللغة: الصينية (الصين) |
| [CHINESE_SINGAPORE](#CHINESE-SINGAPORE) | اللغة: الصينية (سنغافورة) |
| [CHINESE_TAIWAN](#CHINESE-TAIWAN) | اللغة: الصينية (تايوان) |
| [CORSICAN](#CORSICAN) | اللغة: الكورسيكية |
| [CROATIAN](#CROATIAN) | اللغة: الكرواتية |
| [CROATIAN_BOZNIA_AND_HERZEGOVINA](#CROATIAN-BOZNIA-AND-HERZEGOVINA) | اللغة: الكرواتية (البوسنة والهرسك) |
| [CZECH](#CZECH) | اللغة: التشيكية |
| [DANISH](#DANISH) | اللغة: الدنماركية |
| [DIVEHI](#DIVEHI) | اللغة: الديفيهية |
| [DUTCH_BELGIUM](#DUTCH-BELGIUM) | اللغة: الهولندية (بلجيكا) |
| [DUTCH_NETHERLANDS](#DUTCH-NETHERLANDS) | اللغة: الهولندية (هولندا) |
| [EDO](#EDO) | اللغة: إدو |
| [ENGLISH_AUSTRALIA](#ENGLISH-AUSTRALIA) | اللغة: الإنجليزية (أستراليا) |
| [ENGLISH_BELIZE](#ENGLISH-BELIZE) | اللغة: الإنجليزية (بيلز) |
| [ENGLISH_CANADA](#ENGLISH-CANADA) | اللغة: الإنجليزية (كندا) |
| [ENGLISH_CARIBBEAN](#ENGLISH-CARIBBEAN) | اللغة: الإنجليزية (الكاريبي) |
| [ENGLISH_HONG_KONG](#ENGLISH-HONG-KONG) | اللغة: الإنجليزية (هونغ كونغ) |
| [ENGLISH_INDIA](#ENGLISH-INDIA) | اللغة: الإنجليزية (الهند) |
| [ENGLISH_INDONESIA](#ENGLISH-INDONESIA) | اللغة: الإنجليزية (إندونيسيا) |
| [ENGLISH_IRELAND](#ENGLISH-IRELAND) | اللغة: الإنجليزية (إيرلندا) |
| [ENGLISH_JAMAICA](#ENGLISH-JAMAICA) | اللغة: الإنجليزية (جامايكا) |
| [ENGLISH_MALAYSIA](#ENGLISH-MALAYSIA) | اللغة: الإنجليزية (ماليزيا) |
| [ENGLISH_NEW_ZEALAND](#ENGLISH-NEW-ZEALAND) | اللغة: الإنجليزية (نيوزيلندا) |
| [ENGLISH_PHILIPPINES](#ENGLISH-PHILIPPINES) | اللغة: الإنجليزية (الفلبين) |
| [ENGLISH_SINGAPORE](#ENGLISH-SINGAPORE) | اللغة: الإنجليزية (سنغافورة) |
| [ENGLISH_SOUTH_AFRICA](#ENGLISH-SOUTH-AFRICA) | اللغة: الإنجليزية (جنوب أفريقيا) |
| [ENGLISH_TRINIDAD_AND_TOBAGO](#ENGLISH-TRINIDAD-AND-TOBAGO) | اللغة: الإنجليزية (ترينيداد وتوباغو) |
| [ENGLISH_UK](#ENGLISH-UK) | اللغة: الإنجليزية (المملكة المتحدة) |
| [ENGLISH_US](#ENGLISH-US) | اللغة: الإنجليزية (الولايات المتحدة) |
| [ENGLISH_ZIMBABWE](#ENGLISH-ZIMBABWE) | اللغة: الإنجليزية (زمبابوي) |
| [ESTONIAN](#ESTONIAN) | اللغة: الإستونية |
| [FAEROESE](#FAEROESE) | اللغة: الفاروية |
| [FILIPINO](#FILIPINO) | اللغة: الفلبينية |
| [FINNISH](#FINNISH) | اللغة: الفنلندية |
| [FRENCH_BELGIUM](#FRENCH-BELGIUM) | اللغة: الفرنسية (بلجيكا) |
| [FRENCH_CANADA](#FRENCH-CANADA) | اللغة: الفرنسية (كندا) |
| [FRENCH_FRANCE](#FRENCH-FRANCE) | اللغة: الفرنسية (فرنسا) |
| [FRENCH_LUXEMBOURG](#FRENCH-LUXEMBOURG) | اللغة: الفرنسية (لوكسمبورغ) |
| [FRENCH_MONACO](#FRENCH-MONACO) | اللغة: الفرنسية (موناكو) |
| [FRENCH_SWITZERLAND](#FRENCH-SWITZERLAND) | اللغة: الفرنسية (سويسرا) |
| [FRISIAN](#FRISIAN) | اللغة: الفريزية |
| [FULAH_LATIN_SENEGAL](#FULAH-LATIN-SENEGAL) | اللغة: الفولانية (لاتينية، السنغال) |
| [FULAH_NIGERIA](#FULAH-NIGERIA) | اللغة: الفولانية (نيجيريا) |
| [GALICIAN](#GALICIAN) | اللغة: الجاليكية |
| [GEORGIAN](#GEORGIAN) | اللغة: الجورجية |
| [GERMAN_AUSTRIA](#GERMAN-AUSTRIA) | اللغة: الألمانية (النمسا) |
| [GERMAN_GERMANY](#GERMAN-GERMANY) | اللغة: الألمانية (ألمانيا) |
| [GERMAN_LIECHTENSTEIN](#GERMAN-LIECHTENSTEIN) | اللغة: الألمانية (ليختنشتاين) |
| [GERMAN_LUXEMBOURG](#GERMAN-LUXEMBOURG) | اللغة: الألمانية (لوكسمبورغ) |
| [GERMAN_SWITZERLAND](#GERMAN-SWITZERLAND) | اللغة: الألمانية (سويسرا) |
| [GREEK](#GREEK) | اللغة: اليونانية |
| [GREENLANDIC](#GREENLANDIC) | اللغة: الغرينلاندية |
| [GUARANI](#GUARANI) | اللغة: الغوارانية |
| [GUJARATI](#GUJARATI) | اللغة: الغوجاراتية |
| [HAUSA](#HAUSA) | اللغة: الهوسا |
| [HAWAIIAN](#HAWAIIAN) | اللغة: الهاوايية |
| [HEBREW](#HEBREW) | اللغة: العبرية |
| [HINDI](#HINDI) | اللغة: الهندية |
| [HUNGARIAN](#HUNGARIAN) | اللغة: الهنغارية |
| [ICELANDIC](#ICELANDIC) | اللغة: الأيسلندية |
| [IGBO](#IGBO) | اللغة: الإغبو |
| [INARI_SAMI_FINLAND](#INARI-SAMI-FINLAND) | اللغة: الإناري سامي (فنلندا) |
| [INDONESIAN](#INDONESIAN) | اللغة: الإندونيسية |
| [INUKTITUT_LATIN](#INUKTITUT-LATIN) | اللغة: الإينكتيتوت (لاتينية) |
| [INUKTITUT_SYLLABICS](#INUKTITUT-SYLLABICS) | اللغة: الإينكتيتوت (مقاطع) |
| [IRISH](#IRISH) | اللغة: الإيرلندية |
| [ISI_XHOSA](#ISI-XHOSA) | اللغة: الإيسكسوزا |
| [ISI_ZULU](#ISI-ZULU) | اللغة: الإيزولو |
| [ITALIAN_ITALY](#ITALIAN-ITALY) | اللغة: الإيطالية (إيطاليا) |
| [ITALIAN_SWITZERLAND](#ITALIAN-SWITZERLAND) | اللغة: الإيطالية (سويسرا) |
| [JAPANESE](#JAPANESE) | اللغة: اليابانية |
| [KANNADA](#KANNADA) | اللغة: الكانادا |
| [KANURI](#KANURI) | اللغة: الكنوري |
| [KASHMIRI](#KASHMIRI) | اللغة: الكشميرية |
| [KASHMIRI_ARABIC](#KASHMIRI-ARABIC) | اللغة: الكشميرية (العربية) |
| [KAZAKH](#KAZAKH) | اللغة: الكازاخية |
| [KHMER](#KHMER) | اللغة: الخميرية |
| [KICHE](#KICHE) | اللغة: الكيتشي |
| [KINYARWANDA](#KINYARWANDA) | اللغة: الكينيارواندية |
| [KISWAHILI](#KISWAHILI) | اللغة: السواحيلية |
| [KONKANI](#KONKANI) | اللغة: الكونكانية |
| [KOREAN](#KOREAN) | اللغة: الكورية |
| [KYRGYZ](#KYRGYZ) | اللغة: القيرغيزية |
| [LAO](#LAO) | اللغة: اللاوية |
| [LATIN](#LATIN) | اللغة: اللاتينية |
| [LATVIAN](#LATVIAN) | اللغة: اللاتفية |
| [LITHUANIAN](#LITHUANIAN) | اللغة: الليتوانية |
| [LOWER_SORBIAN](#LOWER-SORBIAN) | اللغة: الصربية السفلى |
| [LULE_SAMI_NORWAY](#LULE-SAMI-NORWAY) | اللغة: السامية اللولية (النرويج) |
| [LULE_SAMI_SWEDEN](#LULE-SAMI-SWEDEN) | اللغة: السامية اللولية (السويد) |
| [LUXEMBOUGISH](#LUXEMBOUGISH) | اللغة: اللوكسمبورغية |
| [MACEDONIAN](#MACEDONIAN) | اللغة: المقدونية |
| [MALAYALAM](#MALAYALAM) | اللغة: المالايالامية |
| [MALAY_BRUNEI_DARUSSALAM](#MALAY-BRUNEI-DARUSSALAM) | اللغة: الماليزية (بروناي دار السلام) |
| [MALAY_MALAYSIA](#MALAY-MALAYSIA) | اللغة: الملايو (ماليزيا) |
| [MALTESE](#MALTESE) | اللغة: المالطية |
| [MANIPURI](#MANIPURI) | اللغة: المانيبورية |
| [MAORI](#MAORI) | اللغة: الماورية |
| [MAPUDUNGUN_CHILE](#MAPUDUNGUN-CHILE) | اللغة: مابودونغون (تشيلي) |
| [MARATHI](#MARATHI) | اللغة: الماراثية |
| [MOHAWK](#MOHAWK) | اللغة: المهوك |
| [MONGOLIAN_CYRILLIC](#MONGOLIAN-CYRILLIC) | اللغة: المنغولية (السيريلية) |
| [MONGOLIAN_MONGOLIAN](#MONGOLIAN-MONGOLIAN) | اللغة: المنغولية (المونغولية) |
| [NEPALI](#NEPALI) | اللغة: النيبالية |
| [NORTHERN_SAMI_FINLAND](#NORTHERN-SAMI-FINLAND) | اللغة: السامي الشمالي (فنلندا) |
| [NORTHERN_SAMI_NORWAY](#NORTHERN-SAMI-NORWAY) | اللغة: السامي الشمالي (النرويج) |
| [NORTHERN_SAMI_SWEDEN](#NORTHERN-SAMI-SWEDEN) | اللغة: السامي الشمالي (السويد) |
| [NORWEGIAN_BOKMAL](#NORWEGIAN-BOKMAL) | اللغة: النرويجية بوكمال |
| [NORWEGIAN_NYNORSK](#NORWEGIAN-NYNORSK) | اللغة: النرويجية نينورسك |
| [ORIYA](#ORIYA) | اللغة: الأوريا |
| [OROMO](#OROMO) | اللغة: الأورومو |
| [PAPIAMENTU](#PAPIAMENTU) | اللغة: البابيامنتو |
| [PASHTO](#PASHTO) | اللغة: البشتو |
| [PERSIAN](#PERSIAN) | اللغة: الفارسية |
| [POLISH](#POLISH) | اللغة: البولندية |
| [PORTUGUESE_BRAZIL](#PORTUGUESE-BRAZIL) | اللغة: البرتغالية (البرازيل) |
| [PORTUGUESE_PORTUGAL](#PORTUGUESE-PORTUGAL) | اللغة: البرتغالية (البرتغال) |
| [PUNJABI_INDIA](#PUNJABI-INDIA) | اللغة: البنجابية (الهند) |
| [PUNJABI_PAKISTAN](#PUNJABI-PAKISTAN) | اللغة: البنجابية (باكستان) |
| [QUECHUA_BOLIVIA](#QUECHUA-BOLIVIA) | اللغة: كويتشو (بوليفيا) |
| [QUECHUA_ECUADOR](#QUECHUA-ECUADOR) | اللغة: كويتشو (إكوادور) |
| [QUECHUA_PERU](#QUECHUA-PERU) | اللغة: كويتشو (بيرو) |
| [ROMANIAN](#ROMANIAN) | اللغة: الرومانية |
| [ROMANSH](#ROMANSH) | اللغة: الرومانسية |
| [RUSSIAN](#RUSSIAN) | اللغة: الروسية |
| [SAKHA](#SAKHA) | اللغة: ساخا |
| [SANSKRIT](#SANSKRIT) | اللغة: السنسكريتية |
| [SCOTTISH_GAELIC](#SCOTTISH-GAELIC) | اللغة: الغيلية الاسكتلندية |
| [SERBIAN_CYRILLIC_BOSNIA_AND_HERZEGOVINA](#SERBIAN-CYRILLIC-BOSNIA-AND-HERZEGOVINA) | اللغة: الصربية (سيريلية، البوسنة والهرسك) |
| [SERBIAN_CYRILLIC_SERBIA_AND_MONTENEGRO](#SERBIAN-CYRILLIC-SERBIA-AND-MONTENEGRO) | اللغة: الصربية (سيريلية، صربيا والجبل الأسود) |
| [SERBIAN_LATIN_BOSNIA_AND_HERZEGOVINA](#SERBIAN-LATIN-BOSNIA-AND-HERZEGOVINA) | اللغة: الصربية (لاتينية، البوسنة والهرسك) |
| [SERBIAN_LATIN_SERBIA_AND_MONTENEGRO](#SERBIAN-LATIN-SERBIA-AND-MONTENEGRO) | اللغة: الصربية (لاتينية، صربيا والجبل الأسود) |
| [SINDHI](#SINDHI) | اللغة: السندية |
| [SINDHI_DEVANAGARIC](#SINDHI-DEVANAGARIC) | اللغة: السندية (ديفاناجاري) |
| [SINHALESE](#SINHALESE) | اللغة: السنهالية |
| [SLOVAK](#SLOVAK) | اللغة: السلوفاكية |
| [SLOVENIAN](#SLOVENIAN) | اللغة: السلوفينية |
| [SOMALI](#SOMALI) | اللغة: الصومالية |
| [SORBIAN](#SORBIAN) | اللغة: الصربية العليا |
| [SPANISH_ARGENTINA](#SPANISH-ARGENTINA) | اللغة: الإسبانية (الأرجنتين) |
| [SPANISH_BOLIVIA](#SPANISH-BOLIVIA) | اللغة: الإسبانية (بوليفيا) |
| [SPANISH_CHILE](#SPANISH-CHILE) | اللغة: الإسبانية (تشيلي) |
| [SPANISH_COLOMBIA](#SPANISH-COLOMBIA) | اللغة: الإسبانية (كولومبيا) |
| [SPANISH_COSTA_RICA](#SPANISH-COSTA-RICA) | اللغة: الإسبانية (كوستاريكا) |
| [SPANISH_DOMINICAN_REPUBLIC](#SPANISH-DOMINICAN-REPUBLIC) | اللغة: الإسبانية (جمهورية الدومينيكان) |
| [SPANISH_ECUADOR](#SPANISH-ECUADOR) | اللغة: الإسبانية (الإكوادور) |
| [SPANISH_EL_SALVADOR](#SPANISH-EL-SALVADOR) | اللغة: الإسبانية (السلفادور) |
| [SPANISH_GUATEMALA](#SPANISH-GUATEMALA) | اللغة: الإسبانية (غواتيمالا) |
| [SPANISH_HONDURAS](#SPANISH-HONDURAS) | اللغة: الإسبانية (هندوراس) |
| [SPANISH_MEXICO](#SPANISH-MEXICO) | اللغة: الإسبانية (المكسيك) |
| [SPANISH_NICARAGUA](#SPANISH-NICARAGUA) | اللغة: الإسبانية (نيكاراغوا) |
| [SPANISH_PANAMA](#SPANISH-PANAMA) | اللغة: الإسبانية (بنما) |
| [SPANISH_PARAGUAY](#SPANISH-PARAGUAY) | اللغة: الإسبانية (باراغواي) |
| [SPANISH_PERU](#SPANISH-PERU) | اللغة: الإسبانية (بيرو) |
| [SPANISH_PUERTO_RICO](#SPANISH-PUERTO-RICO) | اللغة: الإسبانية (بورتوريكو) |
| [SPANISH_SPAIN_MODERN_SORT](#SPANISH-SPAIN-MODERN-SORT) | اللغة: الإسبانية (إسبانيا، ترتيب حديث) |
| [SPANISH_SPAIN_TRADITIONAL_SORT](#SPANISH-SPAIN-TRADITIONAL-SORT) | اللغة: الإسبانية (إسبانيا، ترتيب تقليدي) |
| [SPANISH_URUGUAY](#SPANISH-URUGUAY) | اللغة: الإسبانية (أوروغواي) |
| [SPANISH_VENEZUELA](#SPANISH-VENEZUELA) | اللغة: الإسبانية (فنزويلا) |
| [SUTU](#SUTU) | اللغة: سوتو |
| [SWEDISH_FINLAND](#SWEDISH-FINLAND) | اللغة: السويدية (فنلندا) |
| [SWEDISH_SWEDEN](#SWEDISH-SWEDEN) | اللغة: السويدية (السويد) |
| [SYRIAC](#SYRIAC) | اللغة: السريانية |
| [TAJIK](#TAJIK) | اللغة: الطاجيكية |
| [TAMAZIGHT](#TAMAZIGHT) | اللغة: الأمازيغية |
| [TAMAZIGHT_LATIN](#TAMAZIGHT-LATIN) | اللغة: الأمازيغية (لاتينية) |
| [TAMIL](#TAMIL) | اللغة: التاميلية |
| [TATAR](#TATAR) | اللغة: التتارية |
| [TELUGU](#TELUGU) | اللغة: التيلوغو |
| [THAI](#THAI) | اللغة: Thai |
| [TIBETAN_BUTAN](#TIBETAN-BUTAN) | اللغة: Tibetan (Bhutan) |
| [TIBETAN_CHINA](#TIBETAN-CHINA) | اللغة: Tibetan (China) |
| [TIGRIGNA_ERITREA](#TIGRIGNA-ERITREA) | اللغة: Tigrigna (Eritrea) |
| [TIGRIGNA_ETHIOPIA](#TIGRIGNA-ETHIOPIA) | اللغة: Tigrigna (Ethiopia) |
| [TSONGA](#TSONGA) | اللغة: Tsonga |
| [TSWANA](#TSWANA) | اللغة: Tswana |
| [TURKISH](#TURKISH) | اللغة: Turkish |
| [TURKMEN](#TURKMEN) | اللغة: Turkmen |
| [UKRAINIAN](#UKRAINIAN) | اللغة: Ukrainian |
| [URDU](#URDU) | اللغة: Urdu |
| [UZBEK_CYRILLIC](#UZBEK-CYRILLIC) | اللغة: Uzbek (Cyrillic) |
| [UZBEK_LATIN](#UZBEK-LATIN) | اللغة: Uzbek (Latin) |
| [VENDA](#VENDA) | اللغة: Venda |
| [VIETNAMESE](#VIETNAMESE) | اللغة: Vietnamese |
| [WELSH](#WELSH) | اللغة: Welsh |
| [YI](#YI) | اللغة: Yi |
| [YIDDISH](#YIDDISH) | اللغة: Yiddish |
| [YORUBA](#YORUBA) | اللغة: Yoruba |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String editingLanguageName)](#fromName-java.lang.String) |  |
| [getName(int editingLanguage)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int editingLanguage)](#toString-int) |  |
### AFRIKAANS {#AFRIKAANS}
```
public static int AFRIKAANS
```


اللغة: Afrikaans

### ALBANIAN {#ALBANIAN}
```
public static int ALBANIAN
```


اللغة: Albanian

### ALSATIAN {#ALSATIAN}
```
public static int ALSATIAN
```


اللغة: Alsatian

### AMHARIC {#AMHARIC}
```
public static int AMHARIC
```


اللغة: Amharic

### ARABIC_ALGERIA {#ARABIC-ALGERIA}
```
public static int ARABIC_ALGERIA
```


اللغة: Arabic (Algeria)

### ARABIC_BAHRAIN {#ARABIC-BAHRAIN}
```
public static int ARABIC_BAHRAIN
```


اللغة: Arabic (Bahrain)

### ARABIC_EGYPT {#ARABIC-EGYPT}
```
public static int ARABIC_EGYPT
```


اللغة: Arabic (Egypt)

### ARABIC_IRAQ {#ARABIC-IRAQ}
```
public static int ARABIC_IRAQ
```


اللغة: Arabic (Iraq)

### ARABIC_JORDAN {#ARABIC-JORDAN}
```
public static int ARABIC_JORDAN
```


اللغة: العربية (الأردن)

### ARABIC_KUWAIT {#ARABIC-KUWAIT}
```
public static int ARABIC_KUWAIT
```


اللغة: العربية (الكويت)

### ARABIC_LEBANON {#ARABIC-LEBANON}
```
public static int ARABIC_LEBANON
```


اللغة: العربية (لبنان)

### ARABIC_LIBYA {#ARABIC-LIBYA}
```
public static int ARABIC_LIBYA
```


اللغة: العربية (ليبيا)

### ARABIC_MOROCCO {#ARABIC-MOROCCO}
```
public static int ARABIC_MOROCCO
```


اللغة: العربية (المغرب)

### ARABIC_OMAN {#ARABIC-OMAN}
```
public static int ARABIC_OMAN
```


اللغة: العربية (عمان)

### ARABIC_QATAR {#ARABIC-QATAR}
```
public static int ARABIC_QATAR
```


اللغة: العربية (قطر)

### ARABIC_SAUDI_ARABIA {#ARABIC-SAUDI-ARABIA}
```
public static int ARABIC_SAUDI_ARABIA
```


اللغة: العربية (المملكة العربية السعودية)

### ARABIC_SYRIA {#ARABIC-SYRIA}
```
public static int ARABIC_SYRIA
```


اللغة: العربية (سوريا)

### ARABIC_TUNISIA {#ARABIC-TUNISIA}
```
public static int ARABIC_TUNISIA
```


اللغة: العربية (تونس)

### ARABIC_UAE {#ARABIC-UAE}
```
public static int ARABIC_UAE
```


اللغة: العربية (الإمارات العربية المتحدة)

### ARABIC_YEMEN {#ARABIC-YEMEN}
```
public static int ARABIC_YEMEN
```


اللغة: العربية (اليمن)

### ARMENIAN {#ARMENIAN}
```
public static int ARMENIAN
```


اللغة: الأرمنية

### ASSAMESE {#ASSAMESE}
```
public static int ASSAMESE
```


اللغة: الأسامية

### AZERBAIJANI_CYRILLIC {#AZERBAIJANI-CYRILLIC}
```
public static int AZERBAIJANI_CYRILLIC
```


اللغة: الأذربيجانية (سيريلية)

### AZERBAIJANI_LATIN {#AZERBAIJANI-LATIN}
```
public static int AZERBAIJANI_LATIN
```


اللغة: الأذربيجانية (لاتينية)

### BANGLA_BANGLADESH {#BANGLA-BANGLADESH}
```
public static int BANGLA_BANGLADESH
```


اللغة: البنغالية (بنغلاديش)

### BANGLA_INDIA {#BANGLA-INDIA}
```
public static int BANGLA_INDIA
```


اللغة: البنغالية (الهند)

### BASHKIR {#BASHKIR}
```
public static int BASHKIR
```


اللغة: الباشكيرية

### BASQUE {#BASQUE}
```
public static int BASQUE
```


اللغة: الباسكية

### BELARUSIAN {#BELARUSIAN}
```
public static int BELARUSIAN
```


اللغة: البيلاروسية

### BOSNIAN_CYRILLIC {#BOSNIAN-CYRILLIC}
```
public static int BOSNIAN_CYRILLIC
```


اللغة: البوسنية (سيريلية)

### BOSNIAN_LATIN {#BOSNIAN-LATIN}
```
public static int BOSNIAN_LATIN
```


اللغة: البوسنية (لاتينية)

### BRETON {#BRETON}
```
public static int BRETON
```


اللغة: البريتونية

### BULGARIAN {#BULGARIAN}
```
public static int BULGARIAN
```


اللغة: البلغارية

### BURMESE {#BURMESE}
```
public static int BURMESE
```


اللغة: البورمية

### CATALAN {#CATALAN}
```
public static int CATALAN
```


اللغة: الكتالونية

### CENTRAL_KURDISH_IRAQ {#CENTRAL-KURDISH-IRAQ}
```
public static int CENTRAL_KURDISH_IRAQ
```


اللغة: الكردية الوسطى (العراق)

### CHEROKEE {#CHEROKEE}
```
public static int CHEROKEE
```


اللغة: الشيروكي

### CHINESE_HONG_KONG {#CHINESE-HONG-KONG}
```
public static int CHINESE_HONG_KONG
```


اللغة: الصينية (هونغ كونغ)

### CHINESE_MACAO {#CHINESE-MACAO}
```
public static int CHINESE_MACAO
```


اللغة: الصينية (ماكاو)

### CHINESE_PRC {#CHINESE-PRC}
```
public static int CHINESE_PRC
```


اللغة: الصينية (الصين)

### CHINESE_SINGAPORE {#CHINESE-SINGAPORE}
```
public static int CHINESE_SINGAPORE
```


اللغة: الصينية (سنغافورة)

### CHINESE_TAIWAN {#CHINESE-TAIWAN}
```
public static int CHINESE_TAIWAN
```


اللغة: الصينية (تايوان)

### CORSICAN {#CORSICAN}
```
public static int CORSICAN
```


اللغة: الكورسيكية

### CROATIAN {#CROATIAN}
```
public static int CROATIAN
```


اللغة: الكرواتية

### CROATIAN_BOZNIA_AND_HERZEGOVINA {#CROATIAN-BOZNIA-AND-HERZEGOVINA}
```
public static int CROATIAN_BOZNIA_AND_HERZEGOVINA
```


اللغة: الكرواتية (البوسنة والهرسك)

### CZECH {#CZECH}
```
public static int CZECH
```


اللغة: التشيكية

### DANISH {#DANISH}
```
public static int DANISH
```


اللغة: الدنماركية

### DIVEHI {#DIVEHI}
```
public static int DIVEHI
```


اللغة: الديفيهية

### DUTCH_BELGIUM {#DUTCH-BELGIUM}
```
public static int DUTCH_BELGIUM
```


اللغة: الهولندية (بلجيكا)

### DUTCH_NETHERLANDS {#DUTCH-NETHERLANDS}
```
public static int DUTCH_NETHERLANDS
```


اللغة: الهولندية (هولندا)

### EDO {#EDO}
```
public static int EDO
```


اللغة: إدو

### ENGLISH_AUSTRALIA {#ENGLISH-AUSTRALIA}
```
public static int ENGLISH_AUSTRALIA
```


اللغة: الإنجليزية (أستراليا)

### ENGLISH_BELIZE {#ENGLISH-BELIZE}
```
public static int ENGLISH_BELIZE
```


اللغة: الإنجليزية (بيلز)

### ENGLISH_CANADA {#ENGLISH-CANADA}
```
public static int ENGLISH_CANADA
```


اللغة: الإنجليزية (كندا)

### ENGLISH_CARIBBEAN {#ENGLISH-CARIBBEAN}
```
public static int ENGLISH_CARIBBEAN
```


اللغة: الإنجليزية (الكاريبي)

### ENGLISH_HONG_KONG {#ENGLISH-HONG-KONG}
```
public static int ENGLISH_HONG_KONG
```


اللغة: الإنجليزية (هونغ كونغ)

### ENGLISH_INDIA {#ENGLISH-INDIA}
```
public static int ENGLISH_INDIA
```


اللغة: الإنجليزية (الهند)

### ENGLISH_INDONESIA {#ENGLISH-INDONESIA}
```
public static int ENGLISH_INDONESIA
```


اللغة: الإنجليزية (إندونيسيا)

### ENGLISH_IRELAND {#ENGLISH-IRELAND}
```
public static int ENGLISH_IRELAND
```


اللغة: الإنجليزية (إيرلندا)

### ENGLISH_JAMAICA {#ENGLISH-JAMAICA}
```
public static int ENGLISH_JAMAICA
```


اللغة: الإنجليزية (جامايكا)

### ENGLISH_MALAYSIA {#ENGLISH-MALAYSIA}
```
public static int ENGLISH_MALAYSIA
```


اللغة: الإنجليزية (ماليزيا)

### ENGLISH_NEW_ZEALAND {#ENGLISH-NEW-ZEALAND}
```
public static int ENGLISH_NEW_ZEALAND
```


اللغة: الإنجليزية (نيوزيلندا)

### ENGLISH_PHILIPPINES {#ENGLISH-PHILIPPINES}
```
public static int ENGLISH_PHILIPPINES
```


اللغة: الإنجليزية (الفلبين)

### ENGLISH_SINGAPORE {#ENGLISH-SINGAPORE}
```
public static int ENGLISH_SINGAPORE
```


اللغة: الإنجليزية (سنغافورة)

### ENGLISH_SOUTH_AFRICA {#ENGLISH-SOUTH-AFRICA}
```
public static int ENGLISH_SOUTH_AFRICA
```


اللغة: الإنجليزية (جنوب أفريقيا)

### ENGLISH_TRINIDAD_AND_TOBAGO {#ENGLISH-TRINIDAD-AND-TOBAGO}
```
public static int ENGLISH_TRINIDAD_AND_TOBAGO
```


اللغة: الإنجليزية (ترينيداد وتوباغو)

### ENGLISH_UK {#ENGLISH-UK}
```
public static int ENGLISH_UK
```


اللغة: الإنجليزية (المملكة المتحدة)

### ENGLISH_US {#ENGLISH-US}
```
public static int ENGLISH_US
```


اللغة: الإنجليزية (الولايات المتحدة)

### ENGLISH_ZIMBABWE {#ENGLISH-ZIMBABWE}
```
public static int ENGLISH_ZIMBABWE
```


اللغة: الإنجليزية (زمبابوي)

### ESTONIAN {#ESTONIAN}
```
public static int ESTONIAN
```


اللغة: الإستونية

### FAEROESE {#FAEROESE}
```
public static int FAEROESE
```


اللغة: الفاروية

### FILIPINO {#FILIPINO}
```
public static int FILIPINO
```


اللغة: الفلبينية

### FINNISH {#FINNISH}
```
public static int FINNISH
```


اللغة: الفنلندية

### FRENCH_BELGIUM {#FRENCH-BELGIUM}
```
public static int FRENCH_BELGIUM
```


اللغة: الفرنسية (بلجيكا)

### FRENCH_CANADA {#FRENCH-CANADA}
```
public static int FRENCH_CANADA
```


اللغة: الفرنسية (كندا)

### FRENCH_FRANCE {#FRENCH-FRANCE}
```
public static int FRENCH_FRANCE
```


اللغة: الفرنسية (فرنسا)

### FRENCH_LUXEMBOURG {#FRENCH-LUXEMBOURG}
```
public static int FRENCH_LUXEMBOURG
```


اللغة: الفرنسية (لوكسمبورغ)

### FRENCH_MONACO {#FRENCH-MONACO}
```
public static int FRENCH_MONACO
```


اللغة: الفرنسية (موناكو)

### FRENCH_SWITZERLAND {#FRENCH-SWITZERLAND}
```
public static int FRENCH_SWITZERLAND
```


اللغة: الفرنسية (سويسرا)

### FRISIAN {#FRISIAN}
```
public static int FRISIAN
```


اللغة: الفريزية

### FULAH_LATIN_SENEGAL {#FULAH-LATIN-SENEGAL}
```
public static int FULAH_LATIN_SENEGAL
```


اللغة: الفولانية (لاتينية، السنغال)

### FULAH_NIGERIA {#FULAH-NIGERIA}
```
public static int FULAH_NIGERIA
```


اللغة: الفولانية (نيجيريا)

### GALICIAN {#GALICIAN}
```
public static int GALICIAN
```


اللغة: الجاليكية

### GEORGIAN {#GEORGIAN}
```
public static int GEORGIAN
```


اللغة: الجورجية

### GERMAN_AUSTRIA {#GERMAN-AUSTRIA}
```
public static int GERMAN_AUSTRIA
```


اللغة: الألمانية (النمسا)

### GERMAN_GERMANY {#GERMAN-GERMANY}
```
public static int GERMAN_GERMANY
```


اللغة: الألمانية (ألمانيا)

### GERMAN_LIECHTENSTEIN {#GERMAN-LIECHTENSTEIN}
```
public static int GERMAN_LIECHTENSTEIN
```


اللغة: الألمانية (ليختنشتاين)

### GERMAN_LUXEMBOURG {#GERMAN-LUXEMBOURG}
```
public static int GERMAN_LUXEMBOURG
```


اللغة: الألمانية (لوكسمبورغ)

### GERMAN_SWITZERLAND {#GERMAN-SWITZERLAND}
```
public static int GERMAN_SWITZERLAND
```


اللغة: الألمانية (سويسرا)

### GREEK {#GREEK}
```
public static int GREEK
```


اللغة: اليونانية

### GREENLANDIC {#GREENLANDIC}
```
public static int GREENLANDIC
```


اللغة: الغرينلاندية

### GUARANI {#GUARANI}
```
public static int GUARANI
```


اللغة: الغوارانية

### GUJARATI {#GUJARATI}
```
public static int GUJARATI
```


اللغة: الغوجاراتية

### HAUSA {#HAUSA}
```
public static int HAUSA
```


اللغة: الهوسا

### HAWAIIAN {#HAWAIIAN}
```
public static int HAWAIIAN
```


اللغة: الهاوايية

### HEBREW {#HEBREW}
```
public static int HEBREW
```


اللغة: العبرية

### HINDI {#HINDI}
```
public static int HINDI
```


اللغة: الهندية

### HUNGARIAN {#HUNGARIAN}
```
public static int HUNGARIAN
```


اللغة: الهنغارية

### ICELANDIC {#ICELANDIC}
```
public static int ICELANDIC
```


اللغة: الأيسلندية

### IGBO {#IGBO}
```
public static int IGBO
```


اللغة: الإغبو

### INARI_SAMI_FINLAND {#INARI-SAMI-FINLAND}
```
public static int INARI_SAMI_FINLAND
```


اللغة: الإناري سامي (فنلندا)

### INDONESIAN {#INDONESIAN}
```
public static int INDONESIAN
```


اللغة: الإندونيسية

### INUKTITUT_LATIN {#INUKTITUT-LATIN}
```
public static int INUKTITUT_LATIN
```


اللغة: الإينكتيتوت (لاتينية)

### INUKTITUT_SYLLABICS {#INUKTITUT-SYLLABICS}
```
public static int INUKTITUT_SYLLABICS
```


اللغة: الإينكتيتوت (مقاطع)

### IRISH {#IRISH}
```
public static int IRISH
```


اللغة: الإيرلندية

### ISI_XHOSA {#ISI-XHOSA}
```
public static int ISI_XHOSA
```


اللغة: الإيسكسوزا

### ISI_ZULU {#ISI-ZULU}
```
public static int ISI_ZULU
```


اللغة: الإيزولو

### ITALIAN_ITALY {#ITALIAN-ITALY}
```
public static int ITALIAN_ITALY
```


اللغة: الإيطالية (إيطاليا)

### ITALIAN_SWITZERLAND {#ITALIAN-SWITZERLAND}
```
public static int ITALIAN_SWITZERLAND
```


اللغة: الإيطالية (سويسرا)

### JAPANESE {#JAPANESE}
```
public static int JAPANESE
```


اللغة: اليابانية

### KANNADA {#KANNADA}
```
public static int KANNADA
```


اللغة: الكانادا

### KANURI {#KANURI}
```
public static int KANURI
```


اللغة: الكنوري

### KASHMIRI {#KASHMIRI}
```
public static int KASHMIRI
```


اللغة: الكشميرية

### KASHMIRI_ARABIC {#KASHMIRI-ARABIC}
```
public static int KASHMIRI_ARABIC
```


اللغة: الكشميرية (العربية)

### KAZAKH {#KAZAKH}
```
public static int KAZAKH
```


اللغة: الكازاخية

### KHMER {#KHMER}
```
public static int KHMER
```


اللغة: الخميرية

### KICHE {#KICHE}
```
public static int KICHE
```


اللغة: الكيتشي

### KINYARWANDA {#KINYARWANDA}
```
public static int KINYARWANDA
```


اللغة: الكينيارواندية

### KISWAHILI {#KISWAHILI}
```
public static int KISWAHILI
```


اللغة: السواحيلية

### KONKANI {#KONKANI}
```
public static int KONKANI
```


اللغة: الكونكانية

### KOREAN {#KOREAN}
```
public static int KOREAN
```


اللغة: الكورية

### KYRGYZ {#KYRGYZ}
```
public static int KYRGYZ
```


اللغة: القيرغيزية

### LAO {#LAO}
```
public static int LAO
```


اللغة: اللاوية

### LATIN {#LATIN}
```
public static int LATIN
```


اللغة: اللاتينية

### LATVIAN {#LATVIAN}
```
public static int LATVIAN
```


اللغة: اللاتفية

### LITHUANIAN {#LITHUANIAN}
```
public static int LITHUANIAN
```


اللغة: الليتوانية

### LOWER_SORBIAN {#LOWER-SORBIAN}
```
public static int LOWER_SORBIAN
```


اللغة: الصربية السفلى

### LULE_SAMI_NORWAY {#LULE-SAMI-NORWAY}
```
public static int LULE_SAMI_NORWAY
```


اللغة: السامية اللولية (النرويج)

### LULE_SAMI_SWEDEN {#LULE-SAMI-SWEDEN}
```
public static int LULE_SAMI_SWEDEN
```


اللغة: السامية اللولية (السويد)

### LUXEMBOUGISH {#LUXEMBOUGISH}
```
public static int LUXEMBOUGISH
```


اللغة: اللوكسمبورغية

### MACEDONIAN {#MACEDONIAN}
```
public static int MACEDONIAN
```


اللغة: المقدونية

### MALAYALAM {#MALAYALAM}
```
public static int MALAYALAM
```


اللغة: المالايالامية

### MALAY_BRUNEI_DARUSSALAM {#MALAY-BRUNEI-DARUSSALAM}
```
public static int MALAY_BRUNEI_DARUSSALAM
```


اللغة: الماليزية (بروناي دار السلام)

### MALAY_MALAYSIA {#MALAY-MALAYSIA}
```
public static int MALAY_MALAYSIA
```


اللغة: الملايو (ماليزيا)

### MALTESE {#MALTESE}
```
public static int MALTESE
```


اللغة: المالطية

### MANIPURI {#MANIPURI}
```
public static int MANIPURI
```


اللغة: المانيبورية

### MAORI {#MAORI}
```
public static int MAORI
```


اللغة: الماورية

### MAPUDUNGUN_CHILE {#MAPUDUNGUN-CHILE}
```
public static int MAPUDUNGUN_CHILE
```


اللغة: مابودونغون (تشيلي)

### MARATHI {#MARATHI}
```
public static int MARATHI
```


اللغة: الماراثية

### MOHAWK {#MOHAWK}
```
public static int MOHAWK
```


اللغة: المهوك

### MONGOLIAN_CYRILLIC {#MONGOLIAN-CYRILLIC}
```
public static int MONGOLIAN_CYRILLIC
```


اللغة: المنغولية (السيريلية)

### MONGOLIAN_MONGOLIAN {#MONGOLIAN-MONGOLIAN}
```
public static int MONGOLIAN_MONGOLIAN
```


اللغة: المنغولية (المونغولية)

### NEPALI {#NEPALI}
```
public static int NEPALI
```


اللغة: النيبالية

### NORTHERN_SAMI_FINLAND {#NORTHERN-SAMI-FINLAND}
```
public static int NORTHERN_SAMI_FINLAND
```


اللغة: السامي الشمالي (فنلندا)

### NORTHERN_SAMI_NORWAY {#NORTHERN-SAMI-NORWAY}
```
public static int NORTHERN_SAMI_NORWAY
```


اللغة: السامي الشمالي (النرويج)

### NORTHERN_SAMI_SWEDEN {#NORTHERN-SAMI-SWEDEN}
```
public static int NORTHERN_SAMI_SWEDEN
```


اللغة: السامي الشمالي (السويد)

### NORWEGIAN_BOKMAL {#NORWEGIAN-BOKMAL}
```
public static int NORWEGIAN_BOKMAL
```


اللغة: النرويجية بوكمال

### NORWEGIAN_NYNORSK {#NORWEGIAN-NYNORSK}
```
public static int NORWEGIAN_NYNORSK
```


اللغة: النرويجية نينورسك

### ORIYA {#ORIYA}
```
public static int ORIYA
```


اللغة: الأوريا

### OROMO {#OROMO}
```
public static int OROMO
```


اللغة: الأورومو

### PAPIAMENTU {#PAPIAMENTU}
```
public static int PAPIAMENTU
```


اللغة: البابيامنتو

### PASHTO {#PASHTO}
```
public static int PASHTO
```


اللغة: البشتو

### PERSIAN {#PERSIAN}
```
public static int PERSIAN
```


اللغة: الفارسية

### POLISH {#POLISH}
```
public static int POLISH
```


اللغة: البولندية

### PORTUGUESE_BRAZIL {#PORTUGUESE-BRAZIL}
```
public static int PORTUGUESE_BRAZIL
```


اللغة: البرتغالية (البرازيل)

### PORTUGUESE_PORTUGAL {#PORTUGUESE-PORTUGAL}
```
public static int PORTUGUESE_PORTUGAL
```


اللغة: البرتغالية (البرتغال)

### PUNJABI_INDIA {#PUNJABI-INDIA}
```
public static int PUNJABI_INDIA
```


اللغة: البنجابية (الهند)

### PUNJABI_PAKISTAN {#PUNJABI-PAKISTAN}
```
public static int PUNJABI_PAKISTAN
```


اللغة: البنجابية (باكستان)

### QUECHUA_BOLIVIA {#QUECHUA-BOLIVIA}
```
public static int QUECHUA_BOLIVIA
```


اللغة: كويتشو (بوليفيا)

### QUECHUA_ECUADOR {#QUECHUA-ECUADOR}
```
public static int QUECHUA_ECUADOR
```


اللغة: كويتشو (إكوادور)

### QUECHUA_PERU {#QUECHUA-PERU}
```
public static int QUECHUA_PERU
```


اللغة: كويتشو (بيرو)

### ROMANIAN {#ROMANIAN}
```
public static int ROMANIAN
```


اللغة: الرومانية

### ROMANSH {#ROMANSH}
```
public static int ROMANSH
```


اللغة: الرومانسية

### RUSSIAN {#RUSSIAN}
```
public static int RUSSIAN
```


اللغة: الروسية

### SAKHA {#SAKHA}
```
public static int SAKHA
```


اللغة: ساخا

### SANSKRIT {#SANSKRIT}
```
public static int SANSKRIT
```


اللغة: السنسكريتية

### SCOTTISH_GAELIC {#SCOTTISH-GAELIC}
```
public static int SCOTTISH_GAELIC
```


اللغة: الغيلية الاسكتلندية

### SERBIAN_CYRILLIC_BOSNIA_AND_HERZEGOVINA {#SERBIAN-CYRILLIC-BOSNIA-AND-HERZEGOVINA}
```
public static int SERBIAN_CYRILLIC_BOSNIA_AND_HERZEGOVINA
```


اللغة: الصربية (سيريلية، البوسنة والهرسك)

### SERBIAN_CYRILLIC_SERBIA_AND_MONTENEGRO {#SERBIAN-CYRILLIC-SERBIA-AND-MONTENEGRO}
```
public static int SERBIAN_CYRILLIC_SERBIA_AND_MONTENEGRO
```


اللغة: الصربية (سيريلية، صربيا والجبل الأسود)

### SERBIAN_LATIN_BOSNIA_AND_HERZEGOVINA {#SERBIAN-LATIN-BOSNIA-AND-HERZEGOVINA}
```
public static int SERBIAN_LATIN_BOSNIA_AND_HERZEGOVINA
```


اللغة: الصربية (لاتينية، البوسنة والهرسك)

### SERBIAN_LATIN_SERBIA_AND_MONTENEGRO {#SERBIAN-LATIN-SERBIA-AND-MONTENEGRO}
```
public static int SERBIAN_LATIN_SERBIA_AND_MONTENEGRO
```


اللغة: الصربية (لاتينية، صربيا والجبل الأسود)

### SINDHI {#SINDHI}
```
public static int SINDHI
```


اللغة: السندية

### SINDHI_DEVANAGARIC {#SINDHI-DEVANAGARIC}
```
public static int SINDHI_DEVANAGARIC
```


اللغة: السندية (ديفاناجاري)

### SINHALESE {#SINHALESE}
```
public static int SINHALESE
```


اللغة: السنهالية

### SLOVAK {#SLOVAK}
```
public static int SLOVAK
```


اللغة: السلوفاكية

### SLOVENIAN {#SLOVENIAN}
```
public static int SLOVENIAN
```


اللغة: السلوفينية

### SOMALI {#SOMALI}
```
public static int SOMALI
```


اللغة: الصومالية

### SORBIAN {#SORBIAN}
```
public static int SORBIAN
```


اللغة: الصربية العليا

### SPANISH_ARGENTINA {#SPANISH-ARGENTINA}
```
public static int SPANISH_ARGENTINA
```


اللغة: الإسبانية (الأرجنتين)

### SPANISH_BOLIVIA {#SPANISH-BOLIVIA}
```
public static int SPANISH_BOLIVIA
```


اللغة: الإسبانية (بوليفيا)

### SPANISH_CHILE {#SPANISH-CHILE}
```
public static int SPANISH_CHILE
```


اللغة: الإسبانية (تشيلي)

### SPANISH_COLOMBIA {#SPANISH-COLOMBIA}
```
public static int SPANISH_COLOMBIA
```


اللغة: الإسبانية (كولومبيا)

### SPANISH_COSTA_RICA {#SPANISH-COSTA-RICA}
```
public static int SPANISH_COSTA_RICA
```


اللغة: الإسبانية (كوستاريكا)

### SPANISH_DOMINICAN_REPUBLIC {#SPANISH-DOMINICAN-REPUBLIC}
```
public static int SPANISH_DOMINICAN_REPUBLIC
```


اللغة: الإسبانية (جمهورية الدومينيكان)

### SPANISH_ECUADOR {#SPANISH-ECUADOR}
```
public static int SPANISH_ECUADOR
```


اللغة: الإسبانية (الإكوادور)

### SPANISH_EL_SALVADOR {#SPANISH-EL-SALVADOR}
```
public static int SPANISH_EL_SALVADOR
```


اللغة: الإسبانية (السلفادور)

### SPANISH_GUATEMALA {#SPANISH-GUATEMALA}
```
public static int SPANISH_GUATEMALA
```


اللغة: الإسبانية (غواتيمالا)

### SPANISH_HONDURAS {#SPANISH-HONDURAS}
```
public static int SPANISH_HONDURAS
```


اللغة: الإسبانية (هندوراس)

### SPANISH_MEXICO {#SPANISH-MEXICO}
```
public static int SPANISH_MEXICO
```


اللغة: الإسبانية (المكسيك)

### SPANISH_NICARAGUA {#SPANISH-NICARAGUA}
```
public static int SPANISH_NICARAGUA
```


اللغة: الإسبانية (نيكاراغوا)

### SPANISH_PANAMA {#SPANISH-PANAMA}
```
public static int SPANISH_PANAMA
```


اللغة: الإسبانية (بنما)

### SPANISH_PARAGUAY {#SPANISH-PARAGUAY}
```
public static int SPANISH_PARAGUAY
```


اللغة: الإسبانية (باراغواي)

### SPANISH_PERU {#SPANISH-PERU}
```
public static int SPANISH_PERU
```


اللغة: الإسبانية (بيرو)

### SPANISH_PUERTO_RICO {#SPANISH-PUERTO-RICO}
```
public static int SPANISH_PUERTO_RICO
```


اللغة: الإسبانية (بورتوريكو)

### SPANISH_SPAIN_MODERN_SORT {#SPANISH-SPAIN-MODERN-SORT}
```
public static int SPANISH_SPAIN_MODERN_SORT
```


اللغة: الإسبانية (إسبانيا، ترتيب حديث)

### SPANISH_SPAIN_TRADITIONAL_SORT {#SPANISH-SPAIN-TRADITIONAL-SORT}
```
public static int SPANISH_SPAIN_TRADITIONAL_SORT
```


اللغة: الإسبانية (إسبانيا، ترتيب تقليدي)

### SPANISH_URUGUAY {#SPANISH-URUGUAY}
```
public static int SPANISH_URUGUAY
```


اللغة: الإسبانية (أوروغواي)

### SPANISH_VENEZUELA {#SPANISH-VENEZUELA}
```
public static int SPANISH_VENEZUELA
```


اللغة: الإسبانية (فنزويلا)

### SUTU {#SUTU}
```
public static int SUTU
```


اللغة: سوتو

### SWEDISH_FINLAND {#SWEDISH-FINLAND}
```
public static int SWEDISH_FINLAND
```


اللغة: السويدية (فنلندا)

### SWEDISH_SWEDEN {#SWEDISH-SWEDEN}
```
public static int SWEDISH_SWEDEN
```


اللغة: السويدية (السويد)

### SYRIAC {#SYRIAC}
```
public static int SYRIAC
```


اللغة: السريانية

### TAJIK {#TAJIK}
```
public static int TAJIK
```


اللغة: الطاجيكية

### TAMAZIGHT {#TAMAZIGHT}
```
public static int TAMAZIGHT
```


اللغة: الأمازيغية

### TAMAZIGHT_LATIN {#TAMAZIGHT-LATIN}
```
public static int TAMAZIGHT_LATIN
```


اللغة: الأمازيغية (لاتينية)

### TAMIL {#TAMIL}
```
public static int TAMIL
```


اللغة: التاميلية

### TATAR {#TATAR}
```
public static int TATAR
```


اللغة: التتارية

### TELUGU {#TELUGU}
```
public static int TELUGU
```


اللغة: التيلوغو

### THAI {#THAI}
```
public static int THAI
```


اللغة: Thai

### TIBETAN_BUTAN {#TIBETAN-BUTAN}
```
public static int TIBETAN_BUTAN
```


اللغة: Tibetan (Bhutan)

### TIBETAN_CHINA {#TIBETAN-CHINA}
```
public static int TIBETAN_CHINA
```


اللغة: Tibetan (China)

### TIGRIGNA_ERITREA {#TIGRIGNA-ERITREA}
```
public static int TIGRIGNA_ERITREA
```


اللغة: Tigrigna (Eritrea)

### TIGRIGNA_ETHIOPIA {#TIGRIGNA-ETHIOPIA}
```
public static int TIGRIGNA_ETHIOPIA
```


اللغة: Tigrigna (Ethiopia)

### TSONGA {#TSONGA}
```
public static int TSONGA
```


اللغة: Tsonga

### TSWANA {#TSWANA}
```
public static int TSWANA
```


اللغة: Tswana

### TURKISH {#TURKISH}
```
public static int TURKISH
```


اللغة: Turkish

### TURKMEN {#TURKMEN}
```
public static int TURKMEN
```


اللغة: Turkmen

### UKRAINIAN {#UKRAINIAN}
```
public static int UKRAINIAN
```


اللغة: Ukrainian

### URDU {#URDU}
```
public static int URDU
```


اللغة: Urdu

### UZBEK_CYRILLIC {#UZBEK-CYRILLIC}
```
public static int UZBEK_CYRILLIC
```


اللغة: Uzbek (Cyrillic)

### UZBEK_LATIN {#UZBEK-LATIN}
```
public static int UZBEK_LATIN
```


اللغة: Uzbek (Latin)

### VENDA {#VENDA}
```
public static int VENDA
```


اللغة: Venda

### VIETNAMESE {#VIETNAMESE}
```
public static int VIETNAMESE
```


اللغة: Vietnamese

### WELSH {#WELSH}
```
public static int WELSH
```


اللغة: Welsh

### YI {#YI}
```
public static int YI
```


اللغة: Yi

### YIDDISH {#YIDDISH}
```
public static int YIDDISH
```


اللغة: Yiddish

### YORUBA {#YORUBA}
```
public static int YORUBA
```


اللغة: Yoruba

### length {#length}
```
public static int length
```


### fromName(String editingLanguageName) {#fromName-java.lang.String}
```
public static int fromName(String editingLanguageName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| editingLanguageName | java.lang.String |  |

**Returns:**
int
### getName(int editingLanguage) {#getName-int}
```
public static String getName(int editingLanguage)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| editingLanguage | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int editingLanguage) {#toString-int}
```
public static String toString(int editingLanguage)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| editingLanguage | int |  |

**Returns:**
java.lang.String
