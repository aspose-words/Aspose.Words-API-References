---
title: Language
linktitle: Language
second_title: Aspose.Words for Java
description: Specifies the language into which the text will be translated using AI. in Java.
type: docs
weight: 412
url: /java/com.aspose.words/language/
---

**Inheritance:**
java.lang.Object
```
public class Language
```

Specifies the language into which the text will be translated using AI..

 **Examples:** 

Shows how to translate text using Google models.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 String apiKey = System.getenv("API_KEY");
 // Use Google generative language models.
 AiModel model = AiModel.create(AiModelType.GEMINI_FLASH_LATEST).withApiKey(apiKey);

 Document translatedDoc = model.translate(doc, Language.ARABIC);
 translatedDoc.save(getArtifactsDir() + "AI.AiTranslate.docx");
 
```

**M:Aspose.Words.AI.AiModel.Translate(Aspose.Words.Document,Aspose.Words.AI.Language)**
## Fields

| Field | Description |
| --- | --- |
| [AFRIKAANS](#AFRIKAANS) |  |
| [AFRIKAANS_SOUTH_AFRICA](#AFRIKAANS-SOUTH-AFRICA) |  |
| [ALBANIAN](#ALBANIAN) |  |
| [ALBANIAN_ALBANIA](#ALBANIAN-ALBANIA) |  |
| [ALSATIAN](#ALSATIAN) |  |
| [AMHARIC](#AMHARIC) |  |
| [ARABIC](#ARABIC) |  |
| [ARABIC_ALGERIA](#ARABIC-ALGERIA) |  |
| [ARABIC_BAHRAIN](#ARABIC-BAHRAIN) |  |
| [ARABIC_EGYPT](#ARABIC-EGYPT) |  |
| [ARABIC_IRAQ](#ARABIC-IRAQ) |  |
| [ARABIC_JORDAN](#ARABIC-JORDAN) |  |
| [ARABIC_KUWAIT](#ARABIC-KUWAIT) |  |
| [ARABIC_LEBANON](#ARABIC-LEBANON) |  |
| [ARABIC_LIBYA](#ARABIC-LIBYA) |  |
| [ARABIC_MOROCCO](#ARABIC-MOROCCO) |  |
| [ARABIC_OMAN](#ARABIC-OMAN) |  |
| [ARABIC_QATAR](#ARABIC-QATAR) |  |
| [ARABIC_SAUDI_ARABIA](#ARABIC-SAUDI-ARABIA) |  |
| [ARABIC_SYRIA](#ARABIC-SYRIA) |  |
| [ARABIC_TUNISIA](#ARABIC-TUNISIA) |  |
| [ARABIC_UAE](#ARABIC-UAE) |  |
| [ARABIC_YEMEN](#ARABIC-YEMEN) |  |
| [ARMENIAN](#ARMENIAN) |  |
| [ARMENIAN_ARMENIA](#ARMENIAN-ARMENIA) |  |
| [ASSAMESE](#ASSAMESE) |  |
| [AZERI](#AZERI) |  |
| [AZERI_CYRILLIC](#AZERI-CYRILLIC) |  |
| [AZERI_LATIN](#AZERI-LATIN) |  |
| [BASQUE](#BASQUE) |  |
| [BASQUE_BASQUE](#BASQUE-BASQUE) |  |
| [BELARUSIAN](#BELARUSIAN) |  |
| [BELARUSIAN_BELARUS](#BELARUSIAN-BELARUS) |  |
| [BENGALI](#BENGALI) |  |
| [BENGALI_BANGLADESH](#BENGALI-BANGLADESH) |  |
| [BOSNIAN_CYRILLIC](#BOSNIAN-CYRILLIC) |  |
| [BOSNIAN_LATIN](#BOSNIAN-LATIN) |  |
| [BRETON](#BRETON) |  |
| [BULGARIAN](#BULGARIAN) |  |
| [BULGARIAN_BULGARIA](#BULGARIAN-BULGARIA) |  |
| [BURMESE](#BURMESE) |  |
| [CATALAN](#CATALAN) |  |
| [CATALAN_CATALAN](#CATALAN-CATALAN) |  |
| [CHEROKEE](#CHEROKEE) |  |
| [CHINESE_CHINA](#CHINESE-CHINA) |  |
| [CHINESE_HONG_KONG](#CHINESE-HONG-KONG) |  |
| [CHINESE_MACAO](#CHINESE-MACAO) |  |
| [CHINESE_SIMPLIFIED](#CHINESE-SIMPLIFIED) |  |
| [CHINESE_SINGAPORE](#CHINESE-SINGAPORE) |  |
| [CHINESE_TAIWAN](#CHINESE-TAIWAN) |  |
| [CHINESE_TRADITIONAL](#CHINESE-TRADITIONAL) |  |
| [CROATIAN](#CROATIAN) |  |
| [CROATIAN_BOZNIA_AND_HERZEGOVINA](#CROATIAN-BOZNIA-AND-HERZEGOVINA) |  |
| [CROATIAN_CROATIA](#CROATIAN-CROATIA) |  |
| [CZECH](#CZECH) |  |
| [CZECH_CZECH_REPUBLIC](#CZECH-CZECH-REPUBLIC) |  |
| [DANISH](#DANISH) |  |
| [DANISH_DENMARK](#DANISH-DENMARK) |  |
| [DIVEHI](#DIVEHI) |  |
| [DIVEHI_MALDIVES](#DIVEHI-MALDIVES) |  |
| [DUTCH](#DUTCH) |  |
| [DUTCH_BELGIUM](#DUTCH-BELGIUM) |  |
| [DUTCH_NETHERLANDS](#DUTCH-NETHERLANDS) |  |
| [EDO](#EDO) |  |
| [ENGLISH](#ENGLISH) |  |
| [ENGLISH_AUSTRALIA](#ENGLISH-AUSTRALIA) |  |
| [ENGLISH_BELIZE](#ENGLISH-BELIZE) |  |
| [ENGLISH_CANADA](#ENGLISH-CANADA) |  |
| [ENGLISH_CARIBBEAN](#ENGLISH-CARIBBEAN) |  |
| [ENGLISH_HONG_KONG](#ENGLISH-HONG-KONG) |  |
| [ENGLISH_INDIA](#ENGLISH-INDIA) |  |
| [ENGLISH_INDONESIA](#ENGLISH-INDONESIA) |  |
| [ENGLISH_IRELAND](#ENGLISH-IRELAND) |  |
| [ENGLISH_JAMAICA](#ENGLISH-JAMAICA) |  |
| [ENGLISH_MALAYSIA](#ENGLISH-MALAYSIA) |  |
| [ENGLISH_NEW_ZEALAND](#ENGLISH-NEW-ZEALAND) |  |
| [ENGLISH_PHILIPPINES](#ENGLISH-PHILIPPINES) |  |
| [ENGLISH_SINGAPORE](#ENGLISH-SINGAPORE) |  |
| [ENGLISH_SOUTH_AFRICA](#ENGLISH-SOUTH-AFRICA) |  |
| [ENGLISH_TRINIDAD_AND_TOBAGO](#ENGLISH-TRINIDAD-AND-TOBAGO) |  |
| [ENGLISH_UK](#ENGLISH-UK) |  |
| [ENGLISH_US](#ENGLISH-US) |  |
| [ENGLISH_ZIMBABWE](#ENGLISH-ZIMBABWE) |  |
| [ESTONIAN](#ESTONIAN) |  |
| [ESTONIAN_ESTONIA](#ESTONIAN-ESTONIA) |  |
| [FAEROESE](#FAEROESE) |  |
| [FAEROESE_FAROE_ISLANDS](#FAEROESE-FAROE-ISLANDS) |  |
| [FILIPINO](#FILIPINO) |  |
| [FINNISH](#FINNISH) |  |
| [FINNISH_FINLAND](#FINNISH-FINLAND) |  |
| [FRENCH](#FRENCH) |  |
| [FRENCH_BELGIUM](#FRENCH-BELGIUM) |  |
| [FRENCH_CAMEROON](#FRENCH-CAMEROON) |  |
| [FRENCH_CANADA](#FRENCH-CANADA) |  |
| [FRENCH_CONGO](#FRENCH-CONGO) |  |
| [FRENCH_COTE_D_IVOIRE](#FRENCH-COTE-D-IVOIRE) |  |
| [FRENCH_FRANCE](#FRENCH-FRANCE) |  |
| [FRENCH_HAITI](#FRENCH-HAITI) |  |
| [FRENCH_LUXEMBOURG](#FRENCH-LUXEMBOURG) |  |
| [FRENCH_MALI](#FRENCH-MALI) |  |
| [FRENCH_MONACO](#FRENCH-MONACO) |  |
| [FRENCH_MOROCCO](#FRENCH-MOROCCO) |  |
| [FRENCH_REUNION](#FRENCH-REUNION) |  |
| [FRENCH_SENEGAL](#FRENCH-SENEGAL) |  |
| [FRENCH_SWITZERLAND](#FRENCH-SWITZERLAND) |  |
| [FRENCH_WEST_INDIES](#FRENCH-WEST-INDIES) |  |
| [FRISIAN_NETHERLANDS](#FRISIAN-NETHERLANDS) |  |
| [FULFULDE](#FULFULDE) |  |
| [GAELIC_SCOTLAND](#GAELIC-SCOTLAND) |  |
| [GALICIAN](#GALICIAN) |  |
| [GALICIAN_GALICIAN](#GALICIAN-GALICIAN) |  |
| [GEORGIAN](#GEORGIAN) |  |
| [GEORGIAN_GEORGIA](#GEORGIAN-GEORGIA) |  |
| [GERMAN](#GERMAN) |  |
| [GERMAN_AUSTRIA](#GERMAN-AUSTRIA) |  |
| [GERMAN_GERMANY](#GERMAN-GERMANY) |  |
| [GERMAN_LIECHTENSTEIN](#GERMAN-LIECHTENSTEIN) |  |
| [GERMAN_LUXEMBOURG](#GERMAN-LUXEMBOURG) |  |
| [GERMAN_SWITZERLAND](#GERMAN-SWITZERLAND) |  |
| [GREEK](#GREEK) |  |
| [GREEK_GREECE](#GREEK-GREECE) |  |
| [GUARANI](#GUARANI) |  |
| [GUJARATI](#GUJARATI) |  |
| [GUJARATI_INDIA](#GUJARATI-INDIA) |  |
| [HAUSA](#HAUSA) |  |
| [HAWAIIAN](#HAWAIIAN) |  |
| [HEBREW](#HEBREW) |  |
| [HEBREW_ISRAEL](#HEBREW-ISRAEL) |  |
| [HINDI](#HINDI) |  |
| [HINDI_INDIA](#HINDI-INDIA) |  |
| [HUNGARIAN](#HUNGARIAN) |  |
| [HUNGARIAN_HUNGARY](#HUNGARIAN-HUNGARY) |  |
| [IBIBIO](#IBIBIO) |  |
| [ICELANDIC](#ICELANDIC) |  |
| [ICELANDIC_ICELAND](#ICELANDIC-ICELAND) |  |
| [IGBO](#IGBO) |  |
| [INDONESIAN](#INDONESIAN) |  |
| [INDONESIAN_INDONESIA](#INDONESIAN-INDONESIA) |  |
| [INUKTITUT](#INUKTITUT) |  |
| [INUKTITUT_LATIN_CANADA](#INUKTITUT-LATIN-CANADA) |  |
| [IRISH_IRELAND](#IRISH-IRELAND) |  |
| [ITALIAN](#ITALIAN) |  |
| [ITALIAN_ITALY](#ITALIAN-ITALY) |  |
| [ITALIAN_SWITZERLAND](#ITALIAN-SWITZERLAND) |  |
| [JAPANESE](#JAPANESE) |  |
| [JAPANESE_JAPAN](#JAPANESE-JAPAN) |  |
| [KANNADA](#KANNADA) |  |
| [KANNADA_INDIA](#KANNADA-INDIA) |  |
| [KANURI](#KANURI) |  |
| [KASHMIRI](#KASHMIRI) |  |
| [KASHMIRI_ARABIC](#KASHMIRI-ARABIC) |  |
| [KAZAKH](#KAZAKH) |  |
| [KAZAKH_KAZAKHSTAN](#KAZAKH-KAZAKHSTAN) |  |
| [KHMER](#KHMER) |  |
| [KISWAHILI](#KISWAHILI) |  |
| [KISWAHILI_KENYA](#KISWAHILI-KENYA) |  |
| [KONKANI](#KONKANI) |  |
| [KONKANI_INDIA](#KONKANI-INDIA) |  |
| [KOREAN](#KOREAN) |  |
| [KOREAN_KOREA](#KOREAN-KOREA) |  |
| [KYRGYZ](#KYRGYZ) |  |
| [KYRGYZ_KYRGYZSTAN](#KYRGYZ-KYRGYZSTAN) |  |
| [LAO](#LAO) |  |
| [LATIN](#LATIN) |  |
| [LATVIAN](#LATVIAN) |  |
| [LATVIAN_LATVIA](#LATVIAN-LATVIA) |  |
| [LITHUANIAN](#LITHUANIAN) |  |
| [LITHUANIAN_LITHUANIA](#LITHUANIAN-LITHUANIA) |  |
| [LUXEMBOUGISH_LUXEMBURG](#LUXEMBOUGISH-LUXEMBURG) |  |
| [MACEDONIAN](#MACEDONIAN) |  |
| [MACEDONIAN_FYROM](#MACEDONIAN-FYROM) |  |
| [MALAY](#MALAY) |  |
| [MALAYALAM](#MALAYALAM) |  |
| [MALAY_BRUNEI_DARUSSALAM](#MALAY-BRUNEI-DARUSSALAM) |  |
| [MALAY_MALAYSIA](#MALAY-MALAYSIA) |  |
| [MALTESE](#MALTESE) |  |
| [MANIPURI](#MANIPURI) |  |
| [MAORI](#MAORI) |  |
| [MAPUDUNGUN_CHILE](#MAPUDUNGUN-CHILE) |  |
| [MARATHI](#MARATHI) |  |
| [MARATHI_INDIA](#MARATHI-INDIA) |  |
| [MOHAWK_MOHAWK](#MOHAWK-MOHAWK) |  |
| [MONGOLIAN](#MONGOLIAN) |  |
| [MONGOLIAN_CYRILLIC](#MONGOLIAN-CYRILLIC) |  |
| [MONGOLIAN_MONGOLIAN](#MONGOLIAN-MONGOLIAN) |  |
| [NEPALI](#NEPALI) |  |
| [NEPALI_INDIA](#NEPALI-INDIA) |  |
| [NORWEGIAN](#NORWEGIAN) |  |
| [NORWEGIAN_BOKMAL](#NORWEGIAN-BOKMAL) |  |
| [NORWEGIAN_NYNORSK](#NORWEGIAN-NYNORSK) |  |
| [ORIYA](#ORIYA) |  |
| [OROMO](#OROMO) |  |
| [PAPIAMENTU](#PAPIAMENTU) |  |
| [PASHTO](#PASHTO) |  |
| [PERSIAN](#PERSIAN) |  |
| [PERSIAN_IRAN](#PERSIAN-IRAN) |  |
| [POLISH](#POLISH) |  |
| [POLISH_POLAND](#POLISH-POLAND) |  |
| [PORTUGUESE](#PORTUGUESE) |  |
| [PORTUGUESE_BRAZIL](#PORTUGUESE-BRAZIL) |  |
| [PORTUGUESE_PORTUGAL](#PORTUGUESE-PORTUGAL) |  |
| [PUNJABI](#PUNJABI) |  |
| [PUNJABI_INDIA](#PUNJABI-INDIA) |  |
| [PUNJABI_PAKISTAN](#PUNJABI-PAKISTAN) |  |
| [QUECHUA_BOLIVIA](#QUECHUA-BOLIVIA) |  |
| [QUECHUA_ECUADOR](#QUECHUA-ECUADOR) |  |
| [QUECHUA_PERU](#QUECHUA-PERU) |  |
| [ROMANIAN](#ROMANIAN) |  |
| [ROMANIAN_MOLDOVA](#ROMANIAN-MOLDOVA) |  |
| [ROMANIAN_ROMANIA](#ROMANIAN-ROMANIA) |  |
| [ROMANSH_SWITZERLAND](#ROMANSH-SWITZERLAND) |  |
| [RUSSIAN](#RUSSIAN) |  |
| [RUSSIAN_MOLDOVA](#RUSSIAN-MOLDOVA) |  |
| [RUSSIAN_RUSSIA](#RUSSIAN-RUSSIA) |  |
| [SAMI_INARI_FINLAND](#SAMI-INARI-FINLAND) |  |
| [SAMI_LULE_NORWAY](#SAMI-LULE-NORWAY) |  |
| [SAMI_LULE_SWEDEN](#SAMI-LULE-SWEDEN) |  |
| [SAMI_NORTHERN_FINLAND](#SAMI-NORTHERN-FINLAND) |  |
| [SAMI_NORTHERN_NORWAY](#SAMI-NORTHERN-NORWAY) |  |
| [SAMI_NOTHERN_SWEDEN](#SAMI-NOTHERN-SWEDEN) |  |
| [SAMI_SKOLT_FINLAND](#SAMI-SKOLT-FINLAND) |  |
| [SAMI_SOUTHERN_NORWAY](#SAMI-SOUTHERN-NORWAY) |  |
| [SAMI_SOUTHERN_SWEDEN](#SAMI-SOUTHERN-SWEDEN) |  |
| [SANSKRIT](#SANSKRIT) |  |
| [SANSKRIT_INDIA](#SANSKRIT-INDIA) |  |
| [SEPEDI](#SEPEDI) |  |
| [SERBIAN](#SERBIAN) |  |
| [SERBIAN_CYRILLIC_BOSNIA_AND_HERZEGOVINA](#SERBIAN-CYRILLIC-BOSNIA-AND-HERZEGOVINA) |  |
| [SERBIAN_CYRILLIC_SERBIA_AND_MONTENEGRO](#SERBIAN-CYRILLIC-SERBIA-AND-MONTENEGRO) |  |
| [SERBIAN_LATIN_BOSNIA_AND_HERZEGOVINA](#SERBIAN-LATIN-BOSNIA-AND-HERZEGOVINA) |  |
| [SERBIAN_LATIN_SERBIA_AND_MONTENEGRO](#SERBIAN-LATIN-SERBIA-AND-MONTENEGRO) |  |
| [SINDHI](#SINDHI) |  |
| [SINDHI_DEVANAGARIC](#SINDHI-DEVANAGARIC) |  |
| [SINHALESE](#SINHALESE) |  |
| [SLOVAK](#SLOVAK) |  |
| [SLOVAK_SLOVAKIA](#SLOVAK-SLOVAKIA) |  |
| [SLOVENIAN](#SLOVENIAN) |  |
| [SLOVENIAN_SLOVENIA](#SLOVENIAN-SLOVENIA) |  |
| [SOMALI](#SOMALI) |  |
| [SORBIAN](#SORBIAN) |  |
| [SPANISH](#SPANISH) |  |
| [SPANISH_ARGENTINA](#SPANISH-ARGENTINA) |  |
| [SPANISH_BOLIVIA](#SPANISH-BOLIVIA) |  |
| [SPANISH_CHILE](#SPANISH-CHILE) |  |
| [SPANISH_COLOMBIA](#SPANISH-COLOMBIA) |  |
| [SPANISH_COSTA_RICA](#SPANISH-COSTA-RICA) |  |
| [SPANISH_DOMINICAN_REPUBLIC](#SPANISH-DOMINICAN-REPUBLIC) |  |
| [SPANISH_ECUADOR](#SPANISH-ECUADOR) |  |
| [SPANISH_EL_SALVADOR](#SPANISH-EL-SALVADOR) |  |
| [SPANISH_GUATEMALA](#SPANISH-GUATEMALA) |  |
| [SPANISH_HONDURAS](#SPANISH-HONDURAS) |  |
| [SPANISH_MEXICO](#SPANISH-MEXICO) |  |
| [SPANISH_NICARAGUA](#SPANISH-NICARAGUA) |  |
| [SPANISH_PANAMA](#SPANISH-PANAMA) |  |
| [SPANISH_PARAGUAY](#SPANISH-PARAGUAY) |  |
| [SPANISH_PERU](#SPANISH-PERU) |  |
| [SPANISH_PUERTO_RICO](#SPANISH-PUERTO-RICO) |  |
| [SPANISH_SPAIN_MODERN_SORT](#SPANISH-SPAIN-MODERN-SORT) |  |
| [SPANISH_SPAIN_TRADITIONAL_SORT](#SPANISH-SPAIN-TRADITIONAL-SORT) |  |
| [SPANISH_URUGUAY](#SPANISH-URUGUAY) |  |
| [SPANISH_VENEZUELA](#SPANISH-VENEZUELA) |  |
| [SUTU](#SUTU) |  |
| [SWEDISH](#SWEDISH) |  |
| [SWEDISH_FINLAND](#SWEDISH-FINLAND) |  |
| [SWEDISH_SWEDEN](#SWEDISH-SWEDEN) |  |
| [SYRIAC](#SYRIAC) |  |
| [SYRIAC_SYRIA](#SYRIAC-SYRIA) |  |
| [TAJIK](#TAJIK) |  |
| [TAMAZIGHT](#TAMAZIGHT) |  |
| [TAMAZIGHT_LATIN](#TAMAZIGHT-LATIN) |  |
| [TAMIL](#TAMIL) |  |
| [TAMIL_INDIA](#TAMIL-INDIA) |  |
| [TATAR](#TATAR) |  |
| [TATAR_RUSSIA](#TATAR-RUSSIA) |  |
| [TELUGU](#TELUGU) |  |
| [TELUGU_INDIA](#TELUGU-INDIA) |  |
| [THAI](#THAI) |  |
| [THAI_THAILAND](#THAI-THAILAND) |  |
| [TIBETAN_BUTAN](#TIBETAN-BUTAN) |  |
| [TIBETAN_CHINA](#TIBETAN-CHINA) |  |
| [TIGRIGNA_ERITREA](#TIGRIGNA-ERITREA) |  |
| [TIGRIGNA_ETHIOPIA](#TIGRIGNA-ETHIOPIA) |  |
| [TSONGA](#TSONGA) |  |
| [TSWANA](#TSWANA) |  |
| [TURKISH](#TURKISH) |  |
| [TURKISH_TURKEY](#TURKISH-TURKEY) |  |
| [TURKMEN](#TURKMEN) |  |
| [UKRAINIAN](#UKRAINIAN) |  |
| [UKRAINIAN_UKRAINE](#UKRAINIAN-UKRAINE) |  |
| [URDU](#URDU) |  |
| [URDU_INDIAN](#URDU-INDIAN) |  |
| [URDU_PAKISTAN](#URDU-PAKISTAN) |  |
| [UZBEK](#UZBEK) |  |
| [UZBEK_CYRILLIC](#UZBEK-CYRILLIC) |  |
| [UZBEK_LATIN](#UZBEK-LATIN) |  |
| [VENDA](#VENDA) |  |
| [VIETNAMESE](#VIETNAMESE) |  |
| [VIETNAMESE_VIETNAM](#VIETNAMESE-VIETNAM) |  |
| [WELSH](#WELSH) |  |
| [XHOSA](#XHOSA) |  |
| [YI](#YI) |  |
| [YIDDISH](#YIDDISH) |  |
| [YORUBA](#YORUBA) |  |
| [ZULU](#ZULU) |  |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String languageName)](#fromName-java.lang.String) |  |
| [getName(int language)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int language)](#toString-int) |  |
### AFRIKAANS {#AFRIKAANS}
```
public static int AFRIKAANS
```


### AFRIKAANS_SOUTH_AFRICA {#AFRIKAANS-SOUTH-AFRICA}
```
public static int AFRIKAANS_SOUTH_AFRICA
```


### ALBANIAN {#ALBANIAN}
```
public static int ALBANIAN
```


### ALBANIAN_ALBANIA {#ALBANIAN-ALBANIA}
```
public static int ALBANIAN_ALBANIA
```


### ALSATIAN {#ALSATIAN}
```
public static int ALSATIAN
```


### AMHARIC {#AMHARIC}
```
public static int AMHARIC
```


### ARABIC {#ARABIC}
```
public static int ARABIC
```


### ARABIC_ALGERIA {#ARABIC-ALGERIA}
```
public static int ARABIC_ALGERIA
```


### ARABIC_BAHRAIN {#ARABIC-BAHRAIN}
```
public static int ARABIC_BAHRAIN
```


### ARABIC_EGYPT {#ARABIC-EGYPT}
```
public static int ARABIC_EGYPT
```


### ARABIC_IRAQ {#ARABIC-IRAQ}
```
public static int ARABIC_IRAQ
```


### ARABIC_JORDAN {#ARABIC-JORDAN}
```
public static int ARABIC_JORDAN
```


### ARABIC_KUWAIT {#ARABIC-KUWAIT}
```
public static int ARABIC_KUWAIT
```


### ARABIC_LEBANON {#ARABIC-LEBANON}
```
public static int ARABIC_LEBANON
```


### ARABIC_LIBYA {#ARABIC-LIBYA}
```
public static int ARABIC_LIBYA
```


### ARABIC_MOROCCO {#ARABIC-MOROCCO}
```
public static int ARABIC_MOROCCO
```


### ARABIC_OMAN {#ARABIC-OMAN}
```
public static int ARABIC_OMAN
```


### ARABIC_QATAR {#ARABIC-QATAR}
```
public static int ARABIC_QATAR
```


### ARABIC_SAUDI_ARABIA {#ARABIC-SAUDI-ARABIA}
```
public static int ARABIC_SAUDI_ARABIA
```


### ARABIC_SYRIA {#ARABIC-SYRIA}
```
public static int ARABIC_SYRIA
```


### ARABIC_TUNISIA {#ARABIC-TUNISIA}
```
public static int ARABIC_TUNISIA
```


### ARABIC_UAE {#ARABIC-UAE}
```
public static int ARABIC_UAE
```


### ARABIC_YEMEN {#ARABIC-YEMEN}
```
public static int ARABIC_YEMEN
```


### ARMENIAN {#ARMENIAN}
```
public static int ARMENIAN
```


### ARMENIAN_ARMENIA {#ARMENIAN-ARMENIA}
```
public static int ARMENIAN_ARMENIA
```


### ASSAMESE {#ASSAMESE}
```
public static int ASSAMESE
```


### AZERI {#AZERI}
```
public static int AZERI
```


### AZERI_CYRILLIC {#AZERI-CYRILLIC}
```
public static int AZERI_CYRILLIC
```


### AZERI_LATIN {#AZERI-LATIN}
```
public static int AZERI_LATIN
```


### BASQUE {#BASQUE}
```
public static int BASQUE
```


### BASQUE_BASQUE {#BASQUE-BASQUE}
```
public static int BASQUE_BASQUE
```


### BELARUSIAN {#BELARUSIAN}
```
public static int BELARUSIAN
```


### BELARUSIAN_BELARUS {#BELARUSIAN-BELARUS}
```
public static int BELARUSIAN_BELARUS
```


### BENGALI {#BENGALI}
```
public static int BENGALI
```


### BENGALI_BANGLADESH {#BENGALI-BANGLADESH}
```
public static int BENGALI_BANGLADESH
```


### BOSNIAN_CYRILLIC {#BOSNIAN-CYRILLIC}
```
public static int BOSNIAN_CYRILLIC
```


### BOSNIAN_LATIN {#BOSNIAN-LATIN}
```
public static int BOSNIAN_LATIN
```


### BRETON {#BRETON}
```
public static int BRETON
```


### BULGARIAN {#BULGARIAN}
```
public static int BULGARIAN
```


### BULGARIAN_BULGARIA {#BULGARIAN-BULGARIA}
```
public static int BULGARIAN_BULGARIA
```


### BURMESE {#BURMESE}
```
public static int BURMESE
```


### CATALAN {#CATALAN}
```
public static int CATALAN
```


### CATALAN_CATALAN {#CATALAN-CATALAN}
```
public static int CATALAN_CATALAN
```


### CHEROKEE {#CHEROKEE}
```
public static int CHEROKEE
```


### CHINESE_CHINA {#CHINESE-CHINA}
```
public static int CHINESE_CHINA
```


### CHINESE_HONG_KONG {#CHINESE-HONG-KONG}
```
public static int CHINESE_HONG_KONG
```


### CHINESE_MACAO {#CHINESE-MACAO}
```
public static int CHINESE_MACAO
```


### CHINESE_SIMPLIFIED {#CHINESE-SIMPLIFIED}
```
public static int CHINESE_SIMPLIFIED
```


### CHINESE_SINGAPORE {#CHINESE-SINGAPORE}
```
public static int CHINESE_SINGAPORE
```


### CHINESE_TAIWAN {#CHINESE-TAIWAN}
```
public static int CHINESE_TAIWAN
```


### CHINESE_TRADITIONAL {#CHINESE-TRADITIONAL}
```
public static int CHINESE_TRADITIONAL
```


### CROATIAN {#CROATIAN}
```
public static int CROATIAN
```


### CROATIAN_BOZNIA_AND_HERZEGOVINA {#CROATIAN-BOZNIA-AND-HERZEGOVINA}
```
public static int CROATIAN_BOZNIA_AND_HERZEGOVINA
```


### CROATIAN_CROATIA {#CROATIAN-CROATIA}
```
public static int CROATIAN_CROATIA
```


### CZECH {#CZECH}
```
public static int CZECH
```


### CZECH_CZECH_REPUBLIC {#CZECH-CZECH-REPUBLIC}
```
public static int CZECH_CZECH_REPUBLIC
```


### DANISH {#DANISH}
```
public static int DANISH
```


### DANISH_DENMARK {#DANISH-DENMARK}
```
public static int DANISH_DENMARK
```


### DIVEHI {#DIVEHI}
```
public static int DIVEHI
```


### DIVEHI_MALDIVES {#DIVEHI-MALDIVES}
```
public static int DIVEHI_MALDIVES
```


### DUTCH {#DUTCH}
```
public static int DUTCH
```


### DUTCH_BELGIUM {#DUTCH-BELGIUM}
```
public static int DUTCH_BELGIUM
```


### DUTCH_NETHERLANDS {#DUTCH-NETHERLANDS}
```
public static int DUTCH_NETHERLANDS
```


### EDO {#EDO}
```
public static int EDO
```


### ENGLISH {#ENGLISH}
```
public static int ENGLISH
```


### ENGLISH_AUSTRALIA {#ENGLISH-AUSTRALIA}
```
public static int ENGLISH_AUSTRALIA
```


### ENGLISH_BELIZE {#ENGLISH-BELIZE}
```
public static int ENGLISH_BELIZE
```


### ENGLISH_CANADA {#ENGLISH-CANADA}
```
public static int ENGLISH_CANADA
```


### ENGLISH_CARIBBEAN {#ENGLISH-CARIBBEAN}
```
public static int ENGLISH_CARIBBEAN
```


### ENGLISH_HONG_KONG {#ENGLISH-HONG-KONG}
```
public static int ENGLISH_HONG_KONG
```


### ENGLISH_INDIA {#ENGLISH-INDIA}
```
public static int ENGLISH_INDIA
```


### ENGLISH_INDONESIA {#ENGLISH-INDONESIA}
```
public static int ENGLISH_INDONESIA
```


### ENGLISH_IRELAND {#ENGLISH-IRELAND}
```
public static int ENGLISH_IRELAND
```


### ENGLISH_JAMAICA {#ENGLISH-JAMAICA}
```
public static int ENGLISH_JAMAICA
```


### ENGLISH_MALAYSIA {#ENGLISH-MALAYSIA}
```
public static int ENGLISH_MALAYSIA
```


### ENGLISH_NEW_ZEALAND {#ENGLISH-NEW-ZEALAND}
```
public static int ENGLISH_NEW_ZEALAND
```


### ENGLISH_PHILIPPINES {#ENGLISH-PHILIPPINES}
```
public static int ENGLISH_PHILIPPINES
```


### ENGLISH_SINGAPORE {#ENGLISH-SINGAPORE}
```
public static int ENGLISH_SINGAPORE
```


### ENGLISH_SOUTH_AFRICA {#ENGLISH-SOUTH-AFRICA}
```
public static int ENGLISH_SOUTH_AFRICA
```


### ENGLISH_TRINIDAD_AND_TOBAGO {#ENGLISH-TRINIDAD-AND-TOBAGO}
```
public static int ENGLISH_TRINIDAD_AND_TOBAGO
```


### ENGLISH_UK {#ENGLISH-UK}
```
public static int ENGLISH_UK
```


### ENGLISH_US {#ENGLISH-US}
```
public static int ENGLISH_US
```


### ENGLISH_ZIMBABWE {#ENGLISH-ZIMBABWE}
```
public static int ENGLISH_ZIMBABWE
```


### ESTONIAN {#ESTONIAN}
```
public static int ESTONIAN
```


### ESTONIAN_ESTONIA {#ESTONIAN-ESTONIA}
```
public static int ESTONIAN_ESTONIA
```


### FAEROESE {#FAEROESE}
```
public static int FAEROESE
```


### FAEROESE_FAROE_ISLANDS {#FAEROESE-FAROE-ISLANDS}
```
public static int FAEROESE_FAROE_ISLANDS
```


### FILIPINO {#FILIPINO}
```
public static int FILIPINO
```


### FINNISH {#FINNISH}
```
public static int FINNISH
```


### FINNISH_FINLAND {#FINNISH-FINLAND}
```
public static int FINNISH_FINLAND
```


### FRENCH {#FRENCH}
```
public static int FRENCH
```


### FRENCH_BELGIUM {#FRENCH-BELGIUM}
```
public static int FRENCH_BELGIUM
```


### FRENCH_CAMEROON {#FRENCH-CAMEROON}
```
public static int FRENCH_CAMEROON
```


### FRENCH_CANADA {#FRENCH-CANADA}
```
public static int FRENCH_CANADA
```


### FRENCH_CONGO {#FRENCH-CONGO}
```
public static int FRENCH_CONGO
```


### FRENCH_COTE_D_IVOIRE {#FRENCH-COTE-D-IVOIRE}
```
public static int FRENCH_COTE_D_IVOIRE
```


### FRENCH_FRANCE {#FRENCH-FRANCE}
```
public static int FRENCH_FRANCE
```


### FRENCH_HAITI {#FRENCH-HAITI}
```
public static int FRENCH_HAITI
```


### FRENCH_LUXEMBOURG {#FRENCH-LUXEMBOURG}
```
public static int FRENCH_LUXEMBOURG
```


### FRENCH_MALI {#FRENCH-MALI}
```
public static int FRENCH_MALI
```


### FRENCH_MONACO {#FRENCH-MONACO}
```
public static int FRENCH_MONACO
```


### FRENCH_MOROCCO {#FRENCH-MOROCCO}
```
public static int FRENCH_MOROCCO
```


### FRENCH_REUNION {#FRENCH-REUNION}
```
public static int FRENCH_REUNION
```


### FRENCH_SENEGAL {#FRENCH-SENEGAL}
```
public static int FRENCH_SENEGAL
```


### FRENCH_SWITZERLAND {#FRENCH-SWITZERLAND}
```
public static int FRENCH_SWITZERLAND
```


### FRENCH_WEST_INDIES {#FRENCH-WEST-INDIES}
```
public static int FRENCH_WEST_INDIES
```


### FRISIAN_NETHERLANDS {#FRISIAN-NETHERLANDS}
```
public static int FRISIAN_NETHERLANDS
```


### FULFULDE {#FULFULDE}
```
public static int FULFULDE
```


### GAELIC_SCOTLAND {#GAELIC-SCOTLAND}
```
public static int GAELIC_SCOTLAND
```


### GALICIAN {#GALICIAN}
```
public static int GALICIAN
```


### GALICIAN_GALICIAN {#GALICIAN-GALICIAN}
```
public static int GALICIAN_GALICIAN
```


### GEORGIAN {#GEORGIAN}
```
public static int GEORGIAN
```


### GEORGIAN_GEORGIA {#GEORGIAN-GEORGIA}
```
public static int GEORGIAN_GEORGIA
```


### GERMAN {#GERMAN}
```
public static int GERMAN
```


### GERMAN_AUSTRIA {#GERMAN-AUSTRIA}
```
public static int GERMAN_AUSTRIA
```


### GERMAN_GERMANY {#GERMAN-GERMANY}
```
public static int GERMAN_GERMANY
```


### GERMAN_LIECHTENSTEIN {#GERMAN-LIECHTENSTEIN}
```
public static int GERMAN_LIECHTENSTEIN
```


### GERMAN_LUXEMBOURG {#GERMAN-LUXEMBOURG}
```
public static int GERMAN_LUXEMBOURG
```


### GERMAN_SWITZERLAND {#GERMAN-SWITZERLAND}
```
public static int GERMAN_SWITZERLAND
```


### GREEK {#GREEK}
```
public static int GREEK
```


### GREEK_GREECE {#GREEK-GREECE}
```
public static int GREEK_GREECE
```


### GUARANI {#GUARANI}
```
public static int GUARANI
```


### GUJARATI {#GUJARATI}
```
public static int GUJARATI
```


### GUJARATI_INDIA {#GUJARATI-INDIA}
```
public static int GUJARATI_INDIA
```


### HAUSA {#HAUSA}
```
public static int HAUSA
```


### HAWAIIAN {#HAWAIIAN}
```
public static int HAWAIIAN
```


### HEBREW {#HEBREW}
```
public static int HEBREW
```


### HEBREW_ISRAEL {#HEBREW-ISRAEL}
```
public static int HEBREW_ISRAEL
```


### HINDI {#HINDI}
```
public static int HINDI
```


### HINDI_INDIA {#HINDI-INDIA}
```
public static int HINDI_INDIA
```


### HUNGARIAN {#HUNGARIAN}
```
public static int HUNGARIAN
```


### HUNGARIAN_HUNGARY {#HUNGARIAN-HUNGARY}
```
public static int HUNGARIAN_HUNGARY
```


### IBIBIO {#IBIBIO}
```
public static int IBIBIO
```


### ICELANDIC {#ICELANDIC}
```
public static int ICELANDIC
```


### ICELANDIC_ICELAND {#ICELANDIC-ICELAND}
```
public static int ICELANDIC_ICELAND
```


### IGBO {#IGBO}
```
public static int IGBO
```


### INDONESIAN {#INDONESIAN}
```
public static int INDONESIAN
```


### INDONESIAN_INDONESIA {#INDONESIAN-INDONESIA}
```
public static int INDONESIAN_INDONESIA
```


### INUKTITUT {#INUKTITUT}
```
public static int INUKTITUT
```


### INUKTITUT_LATIN_CANADA {#INUKTITUT-LATIN-CANADA}
```
public static int INUKTITUT_LATIN_CANADA
```


### IRISH_IRELAND {#IRISH-IRELAND}
```
public static int IRISH_IRELAND
```


### ITALIAN {#ITALIAN}
```
public static int ITALIAN
```


### ITALIAN_ITALY {#ITALIAN-ITALY}
```
public static int ITALIAN_ITALY
```


### ITALIAN_SWITZERLAND {#ITALIAN-SWITZERLAND}
```
public static int ITALIAN_SWITZERLAND
```


### JAPANESE {#JAPANESE}
```
public static int JAPANESE
```


### JAPANESE_JAPAN {#JAPANESE-JAPAN}
```
public static int JAPANESE_JAPAN
```


### KANNADA {#KANNADA}
```
public static int KANNADA
```


### KANNADA_INDIA {#KANNADA-INDIA}
```
public static int KANNADA_INDIA
```


### KANURI {#KANURI}
```
public static int KANURI
```


### KASHMIRI {#KASHMIRI}
```
public static int KASHMIRI
```


### KASHMIRI_ARABIC {#KASHMIRI-ARABIC}
```
public static int KASHMIRI_ARABIC
```


### KAZAKH {#KAZAKH}
```
public static int KAZAKH
```


### KAZAKH_KAZAKHSTAN {#KAZAKH-KAZAKHSTAN}
```
public static int KAZAKH_KAZAKHSTAN
```


### KHMER {#KHMER}
```
public static int KHMER
```


### KISWAHILI {#KISWAHILI}
```
public static int KISWAHILI
```


### KISWAHILI_KENYA {#KISWAHILI-KENYA}
```
public static int KISWAHILI_KENYA
```


### KONKANI {#KONKANI}
```
public static int KONKANI
```


### KONKANI_INDIA {#KONKANI-INDIA}
```
public static int KONKANI_INDIA
```


### KOREAN {#KOREAN}
```
public static int KOREAN
```


### KOREAN_KOREA {#KOREAN-KOREA}
```
public static int KOREAN_KOREA
```


### KYRGYZ {#KYRGYZ}
```
public static int KYRGYZ
```


### KYRGYZ_KYRGYZSTAN {#KYRGYZ-KYRGYZSTAN}
```
public static int KYRGYZ_KYRGYZSTAN
```


### LAO {#LAO}
```
public static int LAO
```


### LATIN {#LATIN}
```
public static int LATIN
```


### LATVIAN {#LATVIAN}
```
public static int LATVIAN
```


### LATVIAN_LATVIA {#LATVIAN-LATVIA}
```
public static int LATVIAN_LATVIA
```


### LITHUANIAN {#LITHUANIAN}
```
public static int LITHUANIAN
```


### LITHUANIAN_LITHUANIA {#LITHUANIAN-LITHUANIA}
```
public static int LITHUANIAN_LITHUANIA
```


### LUXEMBOUGISH_LUXEMBURG {#LUXEMBOUGISH-LUXEMBURG}
```
public static int LUXEMBOUGISH_LUXEMBURG
```


### MACEDONIAN {#MACEDONIAN}
```
public static int MACEDONIAN
```


### MACEDONIAN_FYROM {#MACEDONIAN-FYROM}
```
public static int MACEDONIAN_FYROM
```


### MALAY {#MALAY}
```
public static int MALAY
```


### MALAYALAM {#MALAYALAM}
```
public static int MALAYALAM
```


### MALAY_BRUNEI_DARUSSALAM {#MALAY-BRUNEI-DARUSSALAM}
```
public static int MALAY_BRUNEI_DARUSSALAM
```


### MALAY_MALAYSIA {#MALAY-MALAYSIA}
```
public static int MALAY_MALAYSIA
```


### MALTESE {#MALTESE}
```
public static int MALTESE
```


### MANIPURI {#MANIPURI}
```
public static int MANIPURI
```


### MAORI {#MAORI}
```
public static int MAORI
```


### MAPUDUNGUN_CHILE {#MAPUDUNGUN-CHILE}
```
public static int MAPUDUNGUN_CHILE
```


### MARATHI {#MARATHI}
```
public static int MARATHI
```


### MARATHI_INDIA {#MARATHI-INDIA}
```
public static int MARATHI_INDIA
```


### MOHAWK_MOHAWK {#MOHAWK-MOHAWK}
```
public static int MOHAWK_MOHAWK
```


### MONGOLIAN {#MONGOLIAN}
```
public static int MONGOLIAN
```


### MONGOLIAN_CYRILLIC {#MONGOLIAN-CYRILLIC}
```
public static int MONGOLIAN_CYRILLIC
```


### MONGOLIAN_MONGOLIAN {#MONGOLIAN-MONGOLIAN}
```
public static int MONGOLIAN_MONGOLIAN
```


### NEPALI {#NEPALI}
```
public static int NEPALI
```


### NEPALI_INDIA {#NEPALI-INDIA}
```
public static int NEPALI_INDIA
```


### NORWEGIAN {#NORWEGIAN}
```
public static int NORWEGIAN
```


### NORWEGIAN_BOKMAL {#NORWEGIAN-BOKMAL}
```
public static int NORWEGIAN_BOKMAL
```


### NORWEGIAN_NYNORSK {#NORWEGIAN-NYNORSK}
```
public static int NORWEGIAN_NYNORSK
```


### ORIYA {#ORIYA}
```
public static int ORIYA
```


### OROMO {#OROMO}
```
public static int OROMO
```


### PAPIAMENTU {#PAPIAMENTU}
```
public static int PAPIAMENTU
```


### PASHTO {#PASHTO}
```
public static int PASHTO
```


### PERSIAN {#PERSIAN}
```
public static int PERSIAN
```


### PERSIAN_IRAN {#PERSIAN-IRAN}
```
public static int PERSIAN_IRAN
```


### POLISH {#POLISH}
```
public static int POLISH
```


### POLISH_POLAND {#POLISH-POLAND}
```
public static int POLISH_POLAND
```


### PORTUGUESE {#PORTUGUESE}
```
public static int PORTUGUESE
```


### PORTUGUESE_BRAZIL {#PORTUGUESE-BRAZIL}
```
public static int PORTUGUESE_BRAZIL
```


### PORTUGUESE_PORTUGAL {#PORTUGUESE-PORTUGAL}
```
public static int PORTUGUESE_PORTUGAL
```


### PUNJABI {#PUNJABI}
```
public static int PUNJABI
```


### PUNJABI_INDIA {#PUNJABI-INDIA}
```
public static int PUNJABI_INDIA
```


### PUNJABI_PAKISTAN {#PUNJABI-PAKISTAN}
```
public static int PUNJABI_PAKISTAN
```


### QUECHUA_BOLIVIA {#QUECHUA-BOLIVIA}
```
public static int QUECHUA_BOLIVIA
```


### QUECHUA_ECUADOR {#QUECHUA-ECUADOR}
```
public static int QUECHUA_ECUADOR
```


### QUECHUA_PERU {#QUECHUA-PERU}
```
public static int QUECHUA_PERU
```


### ROMANIAN {#ROMANIAN}
```
public static int ROMANIAN
```


### ROMANIAN_MOLDOVA {#ROMANIAN-MOLDOVA}
```
public static int ROMANIAN_MOLDOVA
```


### ROMANIAN_ROMANIA {#ROMANIAN-ROMANIA}
```
public static int ROMANIAN_ROMANIA
```


### ROMANSH_SWITZERLAND {#ROMANSH-SWITZERLAND}
```
public static int ROMANSH_SWITZERLAND
```


### RUSSIAN {#RUSSIAN}
```
public static int RUSSIAN
```


### RUSSIAN_MOLDOVA {#RUSSIAN-MOLDOVA}
```
public static int RUSSIAN_MOLDOVA
```


### RUSSIAN_RUSSIA {#RUSSIAN-RUSSIA}
```
public static int RUSSIAN_RUSSIA
```


### SAMI_INARI_FINLAND {#SAMI-INARI-FINLAND}
```
public static int SAMI_INARI_FINLAND
```


### SAMI_LULE_NORWAY {#SAMI-LULE-NORWAY}
```
public static int SAMI_LULE_NORWAY
```


### SAMI_LULE_SWEDEN {#SAMI-LULE-SWEDEN}
```
public static int SAMI_LULE_SWEDEN
```


### SAMI_NORTHERN_FINLAND {#SAMI-NORTHERN-FINLAND}
```
public static int SAMI_NORTHERN_FINLAND
```


### SAMI_NORTHERN_NORWAY {#SAMI-NORTHERN-NORWAY}
```
public static int SAMI_NORTHERN_NORWAY
```


### SAMI_NOTHERN_SWEDEN {#SAMI-NOTHERN-SWEDEN}
```
public static int SAMI_NOTHERN_SWEDEN
```


### SAMI_SKOLT_FINLAND {#SAMI-SKOLT-FINLAND}
```
public static int SAMI_SKOLT_FINLAND
```


### SAMI_SOUTHERN_NORWAY {#SAMI-SOUTHERN-NORWAY}
```
public static int SAMI_SOUTHERN_NORWAY
```


### SAMI_SOUTHERN_SWEDEN {#SAMI-SOUTHERN-SWEDEN}
```
public static int SAMI_SOUTHERN_SWEDEN
```


### SANSKRIT {#SANSKRIT}
```
public static int SANSKRIT
```


### SANSKRIT_INDIA {#SANSKRIT-INDIA}
```
public static int SANSKRIT_INDIA
```


### SEPEDI {#SEPEDI}
```
public static int SEPEDI
```


### SERBIAN {#SERBIAN}
```
public static int SERBIAN
```


### SERBIAN_CYRILLIC_BOSNIA_AND_HERZEGOVINA {#SERBIAN-CYRILLIC-BOSNIA-AND-HERZEGOVINA}
```
public static int SERBIAN_CYRILLIC_BOSNIA_AND_HERZEGOVINA
```


### SERBIAN_CYRILLIC_SERBIA_AND_MONTENEGRO {#SERBIAN-CYRILLIC-SERBIA-AND-MONTENEGRO}
```
public static int SERBIAN_CYRILLIC_SERBIA_AND_MONTENEGRO
```


### SERBIAN_LATIN_BOSNIA_AND_HERZEGOVINA {#SERBIAN-LATIN-BOSNIA-AND-HERZEGOVINA}
```
public static int SERBIAN_LATIN_BOSNIA_AND_HERZEGOVINA
```


### SERBIAN_LATIN_SERBIA_AND_MONTENEGRO {#SERBIAN-LATIN-SERBIA-AND-MONTENEGRO}
```
public static int SERBIAN_LATIN_SERBIA_AND_MONTENEGRO
```


### SINDHI {#SINDHI}
```
public static int SINDHI
```


### SINDHI_DEVANAGARIC {#SINDHI-DEVANAGARIC}
```
public static int SINDHI_DEVANAGARIC
```


### SINHALESE {#SINHALESE}
```
public static int SINHALESE
```


### SLOVAK {#SLOVAK}
```
public static int SLOVAK
```


### SLOVAK_SLOVAKIA {#SLOVAK-SLOVAKIA}
```
public static int SLOVAK_SLOVAKIA
```


### SLOVENIAN {#SLOVENIAN}
```
public static int SLOVENIAN
```


### SLOVENIAN_SLOVENIA {#SLOVENIAN-SLOVENIA}
```
public static int SLOVENIAN_SLOVENIA
```


### SOMALI {#SOMALI}
```
public static int SOMALI
```


### SORBIAN {#SORBIAN}
```
public static int SORBIAN
```


### SPANISH {#SPANISH}
```
public static int SPANISH
```


### SPANISH_ARGENTINA {#SPANISH-ARGENTINA}
```
public static int SPANISH_ARGENTINA
```


### SPANISH_BOLIVIA {#SPANISH-BOLIVIA}
```
public static int SPANISH_BOLIVIA
```


### SPANISH_CHILE {#SPANISH-CHILE}
```
public static int SPANISH_CHILE
```


### SPANISH_COLOMBIA {#SPANISH-COLOMBIA}
```
public static int SPANISH_COLOMBIA
```


### SPANISH_COSTA_RICA {#SPANISH-COSTA-RICA}
```
public static int SPANISH_COSTA_RICA
```


### SPANISH_DOMINICAN_REPUBLIC {#SPANISH-DOMINICAN-REPUBLIC}
```
public static int SPANISH_DOMINICAN_REPUBLIC
```


### SPANISH_ECUADOR {#SPANISH-ECUADOR}
```
public static int SPANISH_ECUADOR
```


### SPANISH_EL_SALVADOR {#SPANISH-EL-SALVADOR}
```
public static int SPANISH_EL_SALVADOR
```


### SPANISH_GUATEMALA {#SPANISH-GUATEMALA}
```
public static int SPANISH_GUATEMALA
```


### SPANISH_HONDURAS {#SPANISH-HONDURAS}
```
public static int SPANISH_HONDURAS
```


### SPANISH_MEXICO {#SPANISH-MEXICO}
```
public static int SPANISH_MEXICO
```


### SPANISH_NICARAGUA {#SPANISH-NICARAGUA}
```
public static int SPANISH_NICARAGUA
```


### SPANISH_PANAMA {#SPANISH-PANAMA}
```
public static int SPANISH_PANAMA
```


### SPANISH_PARAGUAY {#SPANISH-PARAGUAY}
```
public static int SPANISH_PARAGUAY
```


### SPANISH_PERU {#SPANISH-PERU}
```
public static int SPANISH_PERU
```


### SPANISH_PUERTO_RICO {#SPANISH-PUERTO-RICO}
```
public static int SPANISH_PUERTO_RICO
```


### SPANISH_SPAIN_MODERN_SORT {#SPANISH-SPAIN-MODERN-SORT}
```
public static int SPANISH_SPAIN_MODERN_SORT
```


### SPANISH_SPAIN_TRADITIONAL_SORT {#SPANISH-SPAIN-TRADITIONAL-SORT}
```
public static int SPANISH_SPAIN_TRADITIONAL_SORT
```


### SPANISH_URUGUAY {#SPANISH-URUGUAY}
```
public static int SPANISH_URUGUAY
```


### SPANISH_VENEZUELA {#SPANISH-VENEZUELA}
```
public static int SPANISH_VENEZUELA
```


### SUTU {#SUTU}
```
public static int SUTU
```


### SWEDISH {#SWEDISH}
```
public static int SWEDISH
```


### SWEDISH_FINLAND {#SWEDISH-FINLAND}
```
public static int SWEDISH_FINLAND
```


### SWEDISH_SWEDEN {#SWEDISH-SWEDEN}
```
public static int SWEDISH_SWEDEN
```


### SYRIAC {#SYRIAC}
```
public static int SYRIAC
```


### SYRIAC_SYRIA {#SYRIAC-SYRIA}
```
public static int SYRIAC_SYRIA
```


### TAJIK {#TAJIK}
```
public static int TAJIK
```


### TAMAZIGHT {#TAMAZIGHT}
```
public static int TAMAZIGHT
```


### TAMAZIGHT_LATIN {#TAMAZIGHT-LATIN}
```
public static int TAMAZIGHT_LATIN
```


### TAMIL {#TAMIL}
```
public static int TAMIL
```


### TAMIL_INDIA {#TAMIL-INDIA}
```
public static int TAMIL_INDIA
```


### TATAR {#TATAR}
```
public static int TATAR
```


### TATAR_RUSSIA {#TATAR-RUSSIA}
```
public static int TATAR_RUSSIA
```


### TELUGU {#TELUGU}
```
public static int TELUGU
```


### TELUGU_INDIA {#TELUGU-INDIA}
```
public static int TELUGU_INDIA
```


### THAI {#THAI}
```
public static int THAI
```


### THAI_THAILAND {#THAI-THAILAND}
```
public static int THAI_THAILAND
```


### TIBETAN_BUTAN {#TIBETAN-BUTAN}
```
public static int TIBETAN_BUTAN
```


### TIBETAN_CHINA {#TIBETAN-CHINA}
```
public static int TIBETAN_CHINA
```


### TIGRIGNA_ERITREA {#TIGRIGNA-ERITREA}
```
public static int TIGRIGNA_ERITREA
```


### TIGRIGNA_ETHIOPIA {#TIGRIGNA-ETHIOPIA}
```
public static int TIGRIGNA_ETHIOPIA
```


### TSONGA {#TSONGA}
```
public static int TSONGA
```


### TSWANA {#TSWANA}
```
public static int TSWANA
```


### TURKISH {#TURKISH}
```
public static int TURKISH
```


### TURKISH_TURKEY {#TURKISH-TURKEY}
```
public static int TURKISH_TURKEY
```


### TURKMEN {#TURKMEN}
```
public static int TURKMEN
```


### UKRAINIAN {#UKRAINIAN}
```
public static int UKRAINIAN
```


### UKRAINIAN_UKRAINE {#UKRAINIAN-UKRAINE}
```
public static int UKRAINIAN_UKRAINE
```


### URDU {#URDU}
```
public static int URDU
```


### URDU_INDIAN {#URDU-INDIAN}
```
public static int URDU_INDIAN
```


### URDU_PAKISTAN {#URDU-PAKISTAN}
```
public static int URDU_PAKISTAN
```


### UZBEK {#UZBEK}
```
public static int UZBEK
```


### UZBEK_CYRILLIC {#UZBEK-CYRILLIC}
```
public static int UZBEK_CYRILLIC
```


### UZBEK_LATIN {#UZBEK-LATIN}
```
public static int UZBEK_LATIN
```


### VENDA {#VENDA}
```
public static int VENDA
```


### VIETNAMESE {#VIETNAMESE}
```
public static int VIETNAMESE
```


### VIETNAMESE_VIETNAM {#VIETNAMESE-VIETNAM}
```
public static int VIETNAMESE_VIETNAM
```


### WELSH {#WELSH}
```
public static int WELSH
```


### XHOSA {#XHOSA}
```
public static int XHOSA
```


### YI {#YI}
```
public static int YI
```


### YIDDISH {#YIDDISH}
```
public static int YIDDISH
```


### YORUBA {#YORUBA}
```
public static int YORUBA
```


### ZULU {#ZULU}
```
public static int ZULU
```


### length {#length}
```
public static int length
```


### fromName(String languageName) {#fromName-java.lang.String}
```
public static int fromName(String languageName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| languageName | java.lang.String |  |

**Returns:**
int
### getName(int language) {#getName-int}
```
public static String getName(int language)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| language | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int language) {#toString-int}
```
public static String toString(int language)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| language | int |  |

**Returns:**
java.lang.String
