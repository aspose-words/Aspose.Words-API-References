---
title: EditingLanguage
linktitle: EditingLanguage
second_title: Aspose.Words for Java
description: Specifies the editing language in Java.
type: docs
weight: 168
url: /java/com.aspose.words/editinglanguage/
---

**Inheritance:**
java.lang.Object
```
public class EditingLanguage
```

Specifies the editing language.

 **Examples:** 

Shows how to apply language preferences when loading a document.

```

 LoadOptions loadOptions = new LoadOptions();
 loadOptions.getLanguagePreferences().addEditingLanguage(EditingLanguage.JAPANESE);

 Document doc = new Document(getMyDir() + "No default editing language.docx", loadOptions);

 int localeIdFarEast = doc.getStyles().getDefaultFont().getLocaleIdFarEast();
 System.out.println(localeIdFarEast == EditingLanguage.JAPANESE
         ? "The document either has no any FarEast language set in defaults or it was set to Japanese originally."
         : "The document default FarEast language was set to another than Japanese language originally, so it is not overridden.");
 
```
## Fields

| Field | Description |
| --- | --- |
| [AFRIKAANS](#AFRIKAANS) | Language: Afrikaans |
| [ALBANIAN](#ALBANIAN) | Language: Albanian |
| [ALSATIAN](#ALSATIAN) | Language: Alsatian |
| [AMHARIC](#AMHARIC) | Language: Amharic |
| [ARABIC_ALGERIA](#ARABIC-ALGERIA) | Language: Arabic (Algeria) |
| [ARABIC_BAHRAIN](#ARABIC-BAHRAIN) | Language: Arabic (Bahrain) |
| [ARABIC_EGYPT](#ARABIC-EGYPT) | Language: Arabic (Egypt) |
| [ARABIC_IRAQ](#ARABIC-IRAQ) | Language: Arabic (Iraq) |
| [ARABIC_JORDAN](#ARABIC-JORDAN) | Language: Arabic (Jordan) |
| [ARABIC_KUWAIT](#ARABIC-KUWAIT) | Language: Arabic (Kuwait) |
| [ARABIC_LEBANON](#ARABIC-LEBANON) | Language: Arabic (Lebanon) |
| [ARABIC_LIBYA](#ARABIC-LIBYA) | Language: Arabic (Libya) |
| [ARABIC_MOROCCO](#ARABIC-MOROCCO) | Language: Arabic (Morocco) |
| [ARABIC_OMAN](#ARABIC-OMAN) | Language: Arabic (Oman) |
| [ARABIC_QATAR](#ARABIC-QATAR) | Language: Arabic (Qatar) |
| [ARABIC_SAUDI_ARABIA](#ARABIC-SAUDI-ARABIA) | Language: Arabic (Saudi Arabia) |
| [ARABIC_SYRIA](#ARABIC-SYRIA) | Language: Arabic (Syria) |
| [ARABIC_TUNISIA](#ARABIC-TUNISIA) | Language: Arabic (Tunisia) |
| [ARABIC_UAE](#ARABIC-UAE) | Language: Arabic (United Arab Emirates) |
| [ARABIC_YEMEN](#ARABIC-YEMEN) | Language: Arabic (Yemen) |
| [ARMENIAN](#ARMENIAN) | Language: Armenian |
| [ASSAMESE](#ASSAMESE) | Language: Assamese |
| [AZERBAIJANI_CYRILLIC](#AZERBAIJANI-CYRILLIC) | Language: Azerbaijani (Cyrillic) |
| [AZERBAIJANI_LATIN](#AZERBAIJANI-LATIN) | Language: Azerbaijani (Latin) |
| [BANGLA_BANGLADESH](#BANGLA-BANGLADESH) | Language: Bangla (Bangladesh) |
| [BANGLA_INDIA](#BANGLA-INDIA) | Language: Bangla (India) |
| [BASHKIR](#BASHKIR) | Language: Bashkir |
| [BASQUE](#BASQUE) | Language: Basque |
| [BELARUSIAN](#BELARUSIAN) | Language: Belarusian |
| [BOSNIAN_CYRILLIC](#BOSNIAN-CYRILLIC) | Language: Bosnian (Cyrillic) |
| [BOSNIAN_LATIN](#BOSNIAN-LATIN) | Language: Bosnian (Latin) |
| [BRETON](#BRETON) | Language: Breton |
| [BULGARIAN](#BULGARIAN) | Language: Bulgarian |
| [BURMESE](#BURMESE) | Language: Burmese |
| [CATALAN](#CATALAN) | Language: Catalan |
| [CENTRAL_KURDISH_IRAQ](#CENTRAL-KURDISH-IRAQ) | Language: Central Kurdish (Iraq) |
| [CHEROKEE](#CHEROKEE) | Language: Cherokee |
| [CHINESE_HONG_KONG](#CHINESE-HONG-KONG) | Language: Chinese (Hong Kong) |
| [CHINESE_MACAO](#CHINESE-MACAO) | Language: Chinese (Macao) |
| [CHINESE_PRC](#CHINESE-PRC) | Language: Chinese (PRC) |
| [CHINESE_SINGAPORE](#CHINESE-SINGAPORE) | Language: Chinese (Singapore) |
| [CHINESE_TAIWAN](#CHINESE-TAIWAN) | Language: Chinese (Taiwan) |
| [CORSICAN](#CORSICAN) | Language: Corsican |
| [CROATIAN](#CROATIAN) | Language: Croatian |
| [CROATIAN_BOZNIA_AND_HERZEGOVINA](#CROATIAN-BOZNIA-AND-HERZEGOVINA) | Language: Croatian (Bosnia and Herzegovina) |
| [CZECH](#CZECH) | Language: Czech |
| [DANISH](#DANISH) | Language: Danish |
| [DIVEHI](#DIVEHI) | Language: Divehi |
| [DUTCH_BELGIUM](#DUTCH-BELGIUM) | Language: Dutch (Belgium) |
| [DUTCH_NETHERLANDS](#DUTCH-NETHERLANDS) | Language: Dutch (Netherlands) |
| [EDO](#EDO) | Language: Edo |
| [ENGLISH_AUSTRALIA](#ENGLISH-AUSTRALIA) | Language: English (Australia) |
| [ENGLISH_BELIZE](#ENGLISH-BELIZE) | Language: English (Belize) |
| [ENGLISH_CANADA](#ENGLISH-CANADA) | Language: English (Canada) |
| [ENGLISH_CARIBBEAN](#ENGLISH-CARIBBEAN) | Language: English (Caribbean) |
| [ENGLISH_HONG_KONG](#ENGLISH-HONG-KONG) | Language: English (Hong Kong) |
| [ENGLISH_INDIA](#ENGLISH-INDIA) | Language: English (India) |
| [ENGLISH_INDONESIA](#ENGLISH-INDONESIA) | Language: English (Indonesia) |
| [ENGLISH_IRELAND](#ENGLISH-IRELAND) | Language: English (Ireland) |
| [ENGLISH_JAMAICA](#ENGLISH-JAMAICA) | Language: English (Jamaica) |
| [ENGLISH_MALAYSIA](#ENGLISH-MALAYSIA) | Language: English (Malaysia) |
| [ENGLISH_NEW_ZEALAND](#ENGLISH-NEW-ZEALAND) | Language: English (New Zealand) |
| [ENGLISH_PHILIPPINES](#ENGLISH-PHILIPPINES) | Language: English (Philippines) |
| [ENGLISH_SINGAPORE](#ENGLISH-SINGAPORE) | Language: English (Singapore) |
| [ENGLISH_SOUTH_AFRICA](#ENGLISH-SOUTH-AFRICA) | Language: English (South Africa) |
| [ENGLISH_TRINIDAD_AND_TOBAGO](#ENGLISH-TRINIDAD-AND-TOBAGO) | Language: English (Trinidad and Tobago) |
| [ENGLISH_UK](#ENGLISH-UK) | Language: English (UK) |
| [ENGLISH_US](#ENGLISH-US) | Language: English (US) |
| [ENGLISH_ZIMBABWE](#ENGLISH-ZIMBABWE) | Language: English (Zimbabwe) |
| [ESTONIAN](#ESTONIAN) | Language: Estonian |
| [FAEROESE](#FAEROESE) | Language: Faeroese |
| [FILIPINO](#FILIPINO) | Language: Filipino |
| [FINNISH](#FINNISH) | Language: Finnish |
| [FRENCH_BELGIUM](#FRENCH-BELGIUM) | Language: French (Belgium) |
| [FRENCH_CANADA](#FRENCH-CANADA) | Language: French (Canada) |
| [FRENCH_FRANCE](#FRENCH-FRANCE) | Language: French (France) |
| [FRENCH_LUXEMBOURG](#FRENCH-LUXEMBOURG) | Language: French (Luxembourg) |
| [FRENCH_MONACO](#FRENCH-MONACO) | Language: French (Monaco) |
| [FRENCH_SWITZERLAND](#FRENCH-SWITZERLAND) | Language: French (Switzerland) |
| [FRISIAN](#FRISIAN) | Language: Frisian |
| [FULAH_LATIN_SENEGAL](#FULAH-LATIN-SENEGAL) | Language: Fulah (Latin, Senegal) |
| [FULAH_NIGERIA](#FULAH-NIGERIA) | Language: Fulah (Nigeria) |
| [GALICIAN](#GALICIAN) | Language: Galician |
| [GEORGIAN](#GEORGIAN) | Language: Georgian |
| [GERMAN_AUSTRIA](#GERMAN-AUSTRIA) | Language: German (Austria) |
| [GERMAN_GERMANY](#GERMAN-GERMANY) | Language: German (Germany) |
| [GERMAN_LIECHTENSTEIN](#GERMAN-LIECHTENSTEIN) | Language: German (Liechtenstein) |
| [GERMAN_LUXEMBOURG](#GERMAN-LUXEMBOURG) | Language: German (Luxembourg) |
| [GERMAN_SWITZERLAND](#GERMAN-SWITZERLAND) | Language: German (Switzerland) |
| [GREEK](#GREEK) | Language: Greek |
| [GREENLANDIC](#GREENLANDIC) | Language: Greenlandic |
| [GUARANI](#GUARANI) | Language: Guarani |
| [GUJARATI](#GUJARATI) | Language: Gujarati |
| [HAUSA](#HAUSA) | Language: Hausa |
| [HAWAIIAN](#HAWAIIAN) | Language: Hawaiian |
| [HEBREW](#HEBREW) | Language: Hebrew |
| [HINDI](#HINDI) | Language: Hindi |
| [HUNGARIAN](#HUNGARIAN) | Language: Hungarian |
| [ICELANDIC](#ICELANDIC) | Language: Icelandic |
| [IGBO](#IGBO) | Language: Igbo |
| [INARI_SAMI_FINLAND](#INARI-SAMI-FINLAND) | Language: Inari Sami (Finland) |
| [INDONESIAN](#INDONESIAN) | Language: Indonesian |
| [INUKTITUT_LATIN](#INUKTITUT-LATIN) | Language: Inuktitut (Latin) |
| [INUKTITUT_SYLLABICS](#INUKTITUT-SYLLABICS) | Language: Inuktitut (Syllabics) |
| [IRISH](#IRISH) | Language: Irish |
| [ISI_XHOSA](#ISI-XHOSA) | Language: IsiXhosa |
| [ISI_ZULU](#ISI-ZULU) | Language: IsiZulu |
| [ITALIAN_ITALY](#ITALIAN-ITALY) | Language: Italian (Italy) |
| [ITALIAN_SWITZERLAND](#ITALIAN-SWITZERLAND) | Language: Italian (Switzerland) |
| [JAPANESE](#JAPANESE) | Language: Japanese |
| [KANNADA](#KANNADA) | Language: Kannada |
| [KANURI](#KANURI) | Language: Kanuri |
| [KASHMIRI](#KASHMIRI) | Language: Kashmiri |
| [KASHMIRI_ARABIC](#KASHMIRI-ARABIC) | Language: Kashmiri (Arabic) |
| [KAZAKH](#KAZAKH) | Language: Kazakh |
| [KHMER](#KHMER) | Language: Khmer |
| [KICHE](#KICHE) | Language: Kiche |
| [KINYARWANDA](#KINYARWANDA) | Language: Kinyarwanda |
| [KISWAHILI](#KISWAHILI) | Language: Kiswahili |
| [KONKANI](#KONKANI) | Language: Konkani |
| [KOREAN](#KOREAN) | Language: Korean |
| [KYRGYZ](#KYRGYZ) | Language: Kyrgyz |
| [LAO](#LAO) | Language: Lao |
| [LATIN](#LATIN) | Language: Latin |
| [LATVIAN](#LATVIAN) | Language: Latvian |
| [LITHUANIAN](#LITHUANIAN) | Language: Lithuanian |
| [LOWER_SORBIAN](#LOWER-SORBIAN) | Language: Lower Sorbian |
| [LULE_SAMI_NORWAY](#LULE-SAMI-NORWAY) | Language: Lule Sami (Norway) |
| [LULE_SAMI_SWEDEN](#LULE-SAMI-SWEDEN) | Language: Lule Sami (Sweden) |
| [LUXEMBOUGISH](#LUXEMBOUGISH) | Language: Luxembourgish |
| [MACEDONIAN](#MACEDONIAN) | Language: Macedonian |
| [MALAYALAM](#MALAYALAM) | Language: Malayalam |
| [MALAY_BRUNEI_DARUSSALAM](#MALAY-BRUNEI-DARUSSALAM) | Language: Malay (Brunei Darussalam) |
| [MALAY_MALAYSIA](#MALAY-MALAYSIA) | Language: Malay (Malaysia) |
| [MALTESE](#MALTESE) | Language: Maltese |
| [MANIPURI](#MANIPURI) | Language: Manipuri |
| [MAORI](#MAORI) | Language: Maori |
| [MAPUDUNGUN_CHILE](#MAPUDUNGUN-CHILE) | Language: Mapudungun (Chile) |
| [MARATHI](#MARATHI) | Language: Marathi |
| [MOHAWK](#MOHAWK) | Language: Mohawk |
| [MONGOLIAN_CYRILLIC](#MONGOLIAN-CYRILLIC) | Language: Mongolian (Cyrillic) |
| [MONGOLIAN_MONGOLIAN](#MONGOLIAN-MONGOLIAN) | Language: Mongolian (Mongolian) |
| [NEPALI](#NEPALI) | Language: Nepali |
| [NORTHERN_SAMI_FINLAND](#NORTHERN-SAMI-FINLAND) | Language: Northern Sami (Finland) |
| [NORTHERN_SAMI_NORWAY](#NORTHERN-SAMI-NORWAY) | Language: Northern Sami (Norway) |
| [NORTHERN_SAMI_SWEDEN](#NORTHERN-SAMI-SWEDEN) | Language: Northern Sami (Sweden) |
| [NORWEGIAN_BOKMAL](#NORWEGIAN-BOKMAL) | Language: Norwegian Bokmal |
| [NORWEGIAN_NYNORSK](#NORWEGIAN-NYNORSK) | Language: Norwegian Nynorsk |
| [ORIYA](#ORIYA) | Language: Oriya |
| [OROMO](#OROMO) | Language: Oromo |
| [PAPIAMENTU](#PAPIAMENTU) | Language: Papiamentu |
| [PASHTO](#PASHTO) | Language: Pashto |
| [PERSIAN](#PERSIAN) | Language: Persian |
| [POLISH](#POLISH) | Language: Polish |
| [PORTUGUESE_BRAZIL](#PORTUGUESE-BRAZIL) | Language: Portuguese (Brazil) |
| [PORTUGUESE_PORTUGAL](#PORTUGUESE-PORTUGAL) | Language: Portuguese (Portugal) |
| [PUNJABI_INDIA](#PUNJABI-INDIA) | Language: Punjabi (India) |
| [PUNJABI_PAKISTAN](#PUNJABI-PAKISTAN) | Language: Punjabi (Pakistan) |
| [QUECHUA_BOLIVIA](#QUECHUA-BOLIVIA) | Language: Quechua (Bolivia) |
| [QUECHUA_ECUADOR](#QUECHUA-ECUADOR) | Language: Quechua (Ecuador) |
| [QUECHUA_PERU](#QUECHUA-PERU) | Language: Quechua (Peru) |
| [ROMANIAN](#ROMANIAN) | Language: Romanian |
| [ROMANSH](#ROMANSH) | Language: Romansh |
| [RUSSIAN](#RUSSIAN) | Language: Russian |
| [SAKHA](#SAKHA) | Language: Sakha |
| [SANSKRIT](#SANSKRIT) | Language: Sanskrit |
| [SCOTTISH_GAELIC](#SCOTTISH-GAELIC) | Language: Scottish Gaelic |
| [SERBIAN_CYRILLIC_BOSNIA_AND_HERZEGOVINA](#SERBIAN-CYRILLIC-BOSNIA-AND-HERZEGOVINA) | Language: Serbian (Cyrillic, Bosnia and Herzegovina) |
| [SERBIAN_CYRILLIC_SERBIA_AND_MONTENEGRO](#SERBIAN-CYRILLIC-SERBIA-AND-MONTENEGRO) | Language: Serbian (Cyrillic, Serbia and Montenegro) |
| [SERBIAN_LATIN_BOSNIA_AND_HERZEGOVINA](#SERBIAN-LATIN-BOSNIA-AND-HERZEGOVINA) | Language: Serbian (Latin, Bosnia and Herzegovina) |
| [SERBIAN_LATIN_SERBIA_AND_MONTENEGRO](#SERBIAN-LATIN-SERBIA-AND-MONTENEGRO) | Language: Serbian (Latin, Serbia and Montenegro) |
| [SINDHI](#SINDHI) | Language: Sindhi |
| [SINDHI_DEVANAGARIC](#SINDHI-DEVANAGARIC) | Language: Sindhi (Devanagari) |
| [SINHALESE](#SINHALESE) | Language: Sinhalese |
| [SLOVAK](#SLOVAK) | Language: Slovak |
| [SLOVENIAN](#SLOVENIAN) | Language: Slovenian |
| [SOMALI](#SOMALI) | Language: Somali |
| [SORBIAN](#SORBIAN) | Language: Sorbian |
| [SPANISH_ARGENTINA](#SPANISH-ARGENTINA) | Language: Spanish (Argentina) |
| [SPANISH_BOLIVIA](#SPANISH-BOLIVIA) | Language: Spanish (Bolivia) |
| [SPANISH_CHILE](#SPANISH-CHILE) | Language: Spanish (Chile) |
| [SPANISH_COLOMBIA](#SPANISH-COLOMBIA) | Language: Spanish (Colombia) |
| [SPANISH_COSTA_RICA](#SPANISH-COSTA-RICA) | Language: Spanish (Costa Rica) |
| [SPANISH_DOMINICAN_REPUBLIC](#SPANISH-DOMINICAN-REPUBLIC) | Language: Spanish (Dominican Republic) |
| [SPANISH_ECUADOR](#SPANISH-ECUADOR) | Language: Spanish (Ecuador) |
| [SPANISH_EL_SALVADOR](#SPANISH-EL-SALVADOR) | Language: Spanish (El Salvador) |
| [SPANISH_GUATEMALA](#SPANISH-GUATEMALA) | Language: Spanish (Guatemala) |
| [SPANISH_HONDURAS](#SPANISH-HONDURAS) | Language: Spanish (Honduras) |
| [SPANISH_MEXICO](#SPANISH-MEXICO) | Language: Spanish (Mexico) |
| [SPANISH_NICARAGUA](#SPANISH-NICARAGUA) | Language: Spanish (Nicaragua) |
| [SPANISH_PANAMA](#SPANISH-PANAMA) | Language: Spanish (Panama) |
| [SPANISH_PARAGUAY](#SPANISH-PARAGUAY) | Language: Spanish (Paraguay) |
| [SPANISH_PERU](#SPANISH-PERU) | Language: Spanish (Peru) |
| [SPANISH_PUERTO_RICO](#SPANISH-PUERTO-RICO) | Language: Spanish (Puerto Rico) |
| [SPANISH_SPAIN_MODERN_SORT](#SPANISH-SPAIN-MODERN-SORT) | Language: Spanish (Spain, Modern Sort) |
| [SPANISH_SPAIN_TRADITIONAL_SORT](#SPANISH-SPAIN-TRADITIONAL-SORT) | Language: Spanish (Spain, Traditional Sort) |
| [SPANISH_URUGUAY](#SPANISH-URUGUAY) | Language: Spanish (Uruguay) |
| [SPANISH_VENEZUELA](#SPANISH-VENEZUELA) | Language: Spanish (Venezuela) |
| [SUTU](#SUTU) | Language: Sutu |
| [SWEDISH_FINLAND](#SWEDISH-FINLAND) | Language: Swedish (Finland) |
| [SWEDISH_SWEDEN](#SWEDISH-SWEDEN) | Language: Swedish (Sweden) |
| [SYRIAC](#SYRIAC) | Language: Syriac |
| [TAJIK](#TAJIK) | Language: Tajik |
| [TAMAZIGHT](#TAMAZIGHT) | Language: Tamazight |
| [TAMAZIGHT_LATIN](#TAMAZIGHT-LATIN) | Language: Tamazight (Latin) |
| [TAMIL](#TAMIL) | Language: Tamil |
| [TATAR](#TATAR) | Language: Tatar |
| [TELUGU](#TELUGU) | Language: Telugu |
| [THAI](#THAI) | Language: Thai |
| [TIBETAN_BUTAN](#TIBETAN-BUTAN) | Language: Tibetan (Bhutan) |
| [TIBETAN_CHINA](#TIBETAN-CHINA) | Language: Tibetan (China) |
| [TIGRIGNA_ERITREA](#TIGRIGNA-ERITREA) | Language: Tigrigna (Eritrea) |
| [TIGRIGNA_ETHIOPIA](#TIGRIGNA-ETHIOPIA) | Language: Tigrigna (Ethiopia) |
| [TSONGA](#TSONGA) | Language: Tsonga |
| [TSWANA](#TSWANA) | Language: Tswana |
| [TURKISH](#TURKISH) | Language: Turkish |
| [TURKMEN](#TURKMEN) | Language: Turkmen |
| [UKRAINIAN](#UKRAINIAN) | Language: Ukrainian |
| [URDU](#URDU) | Language: Urdu |
| [UZBEK_CYRILLIC](#UZBEK-CYRILLIC) | Language: Uzbek (Cyrillic) |
| [UZBEK_LATIN](#UZBEK-LATIN) | Language: Uzbek (Latin) |
| [VENDA](#VENDA) | Language: Venda |
| [VIETNAMESE](#VIETNAMESE) | Language: Vietnamese |
| [WELSH](#WELSH) | Language: Welsh |
| [YI](#YI) | Language: Yi |
| [YIDDISH](#YIDDISH) | Language: Yiddish |
| [YORUBA](#YORUBA) | Language: Yoruba |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String editingLanguageName)](#fromName-java.lang.String) |  |
| [getName(int editingLanguage)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int editingLanguage)](#toString-int) |  |
### AFRIKAANS {#AFRIKAANS}
```
public static int AFRIKAANS
```


Language: Afrikaans

### ALBANIAN {#ALBANIAN}
```
public static int ALBANIAN
```


Language: Albanian

### ALSATIAN {#ALSATIAN}
```
public static int ALSATIAN
```


Language: Alsatian

### AMHARIC {#AMHARIC}
```
public static int AMHARIC
```


Language: Amharic

### ARABIC_ALGERIA {#ARABIC-ALGERIA}
```
public static int ARABIC_ALGERIA
```


Language: Arabic (Algeria)

### ARABIC_BAHRAIN {#ARABIC-BAHRAIN}
```
public static int ARABIC_BAHRAIN
```


Language: Arabic (Bahrain)

### ARABIC_EGYPT {#ARABIC-EGYPT}
```
public static int ARABIC_EGYPT
```


Language: Arabic (Egypt)

### ARABIC_IRAQ {#ARABIC-IRAQ}
```
public static int ARABIC_IRAQ
```


Language: Arabic (Iraq)

### ARABIC_JORDAN {#ARABIC-JORDAN}
```
public static int ARABIC_JORDAN
```


Language: Arabic (Jordan)

### ARABIC_KUWAIT {#ARABIC-KUWAIT}
```
public static int ARABIC_KUWAIT
```


Language: Arabic (Kuwait)

### ARABIC_LEBANON {#ARABIC-LEBANON}
```
public static int ARABIC_LEBANON
```


Language: Arabic (Lebanon)

### ARABIC_LIBYA {#ARABIC-LIBYA}
```
public static int ARABIC_LIBYA
```


Language: Arabic (Libya)

### ARABIC_MOROCCO {#ARABIC-MOROCCO}
```
public static int ARABIC_MOROCCO
```


Language: Arabic (Morocco)

### ARABIC_OMAN {#ARABIC-OMAN}
```
public static int ARABIC_OMAN
```


Language: Arabic (Oman)

### ARABIC_QATAR {#ARABIC-QATAR}
```
public static int ARABIC_QATAR
```


Language: Arabic (Qatar)

### ARABIC_SAUDI_ARABIA {#ARABIC-SAUDI-ARABIA}
```
public static int ARABIC_SAUDI_ARABIA
```


Language: Arabic (Saudi Arabia)

### ARABIC_SYRIA {#ARABIC-SYRIA}
```
public static int ARABIC_SYRIA
```


Language: Arabic (Syria)

### ARABIC_TUNISIA {#ARABIC-TUNISIA}
```
public static int ARABIC_TUNISIA
```


Language: Arabic (Tunisia)

### ARABIC_UAE {#ARABIC-UAE}
```
public static int ARABIC_UAE
```


Language: Arabic (United Arab Emirates)

### ARABIC_YEMEN {#ARABIC-YEMEN}
```
public static int ARABIC_YEMEN
```


Language: Arabic (Yemen)

### ARMENIAN {#ARMENIAN}
```
public static int ARMENIAN
```


Language: Armenian

### ASSAMESE {#ASSAMESE}
```
public static int ASSAMESE
```


Language: Assamese

### AZERBAIJANI_CYRILLIC {#AZERBAIJANI-CYRILLIC}
```
public static int AZERBAIJANI_CYRILLIC
```


Language: Azerbaijani (Cyrillic)

### AZERBAIJANI_LATIN {#AZERBAIJANI-LATIN}
```
public static int AZERBAIJANI_LATIN
```


Language: Azerbaijani (Latin)

### BANGLA_BANGLADESH {#BANGLA-BANGLADESH}
```
public static int BANGLA_BANGLADESH
```


Language: Bangla (Bangladesh)

### BANGLA_INDIA {#BANGLA-INDIA}
```
public static int BANGLA_INDIA
```


Language: Bangla (India)

### BASHKIR {#BASHKIR}
```
public static int BASHKIR
```


Language: Bashkir

### BASQUE {#BASQUE}
```
public static int BASQUE
```


Language: Basque

### BELARUSIAN {#BELARUSIAN}
```
public static int BELARUSIAN
```


Language: Belarusian

### BOSNIAN_CYRILLIC {#BOSNIAN-CYRILLIC}
```
public static int BOSNIAN_CYRILLIC
```


Language: Bosnian (Cyrillic)

### BOSNIAN_LATIN {#BOSNIAN-LATIN}
```
public static int BOSNIAN_LATIN
```


Language: Bosnian (Latin)

### BRETON {#BRETON}
```
public static int BRETON
```


Language: Breton

### BULGARIAN {#BULGARIAN}
```
public static int BULGARIAN
```


Language: Bulgarian

### BURMESE {#BURMESE}
```
public static int BURMESE
```


Language: Burmese

### CATALAN {#CATALAN}
```
public static int CATALAN
```


Language: Catalan

### CENTRAL_KURDISH_IRAQ {#CENTRAL-KURDISH-IRAQ}
```
public static int CENTRAL_KURDISH_IRAQ
```


Language: Central Kurdish (Iraq)

### CHEROKEE {#CHEROKEE}
```
public static int CHEROKEE
```


Language: Cherokee

### CHINESE_HONG_KONG {#CHINESE-HONG-KONG}
```
public static int CHINESE_HONG_KONG
```


Language: Chinese (Hong Kong)

### CHINESE_MACAO {#CHINESE-MACAO}
```
public static int CHINESE_MACAO
```


Language: Chinese (Macao)

### CHINESE_PRC {#CHINESE-PRC}
```
public static int CHINESE_PRC
```


Language: Chinese (PRC)

### CHINESE_SINGAPORE {#CHINESE-SINGAPORE}
```
public static int CHINESE_SINGAPORE
```


Language: Chinese (Singapore)

### CHINESE_TAIWAN {#CHINESE-TAIWAN}
```
public static int CHINESE_TAIWAN
```


Language: Chinese (Taiwan)

### CORSICAN {#CORSICAN}
```
public static int CORSICAN
```


Language: Corsican

### CROATIAN {#CROATIAN}
```
public static int CROATIAN
```


Language: Croatian

### CROATIAN_BOZNIA_AND_HERZEGOVINA {#CROATIAN-BOZNIA-AND-HERZEGOVINA}
```
public static int CROATIAN_BOZNIA_AND_HERZEGOVINA
```


Language: Croatian (Bosnia and Herzegovina)

### CZECH {#CZECH}
```
public static int CZECH
```


Language: Czech

### DANISH {#DANISH}
```
public static int DANISH
```


Language: Danish

### DIVEHI {#DIVEHI}
```
public static int DIVEHI
```


Language: Divehi

### DUTCH_BELGIUM {#DUTCH-BELGIUM}
```
public static int DUTCH_BELGIUM
```


Language: Dutch (Belgium)

### DUTCH_NETHERLANDS {#DUTCH-NETHERLANDS}
```
public static int DUTCH_NETHERLANDS
```


Language: Dutch (Netherlands)

### EDO {#EDO}
```
public static int EDO
```


Language: Edo

### ENGLISH_AUSTRALIA {#ENGLISH-AUSTRALIA}
```
public static int ENGLISH_AUSTRALIA
```


Language: English (Australia)

### ENGLISH_BELIZE {#ENGLISH-BELIZE}
```
public static int ENGLISH_BELIZE
```


Language: English (Belize)

### ENGLISH_CANADA {#ENGLISH-CANADA}
```
public static int ENGLISH_CANADA
```


Language: English (Canada)

### ENGLISH_CARIBBEAN {#ENGLISH-CARIBBEAN}
```
public static int ENGLISH_CARIBBEAN
```


Language: English (Caribbean)

### ENGLISH_HONG_KONG {#ENGLISH-HONG-KONG}
```
public static int ENGLISH_HONG_KONG
```


Language: English (Hong Kong)

### ENGLISH_INDIA {#ENGLISH-INDIA}
```
public static int ENGLISH_INDIA
```


Language: English (India)

### ENGLISH_INDONESIA {#ENGLISH-INDONESIA}
```
public static int ENGLISH_INDONESIA
```


Language: English (Indonesia)

### ENGLISH_IRELAND {#ENGLISH-IRELAND}
```
public static int ENGLISH_IRELAND
```


Language: English (Ireland)

### ENGLISH_JAMAICA {#ENGLISH-JAMAICA}
```
public static int ENGLISH_JAMAICA
```


Language: English (Jamaica)

### ENGLISH_MALAYSIA {#ENGLISH-MALAYSIA}
```
public static int ENGLISH_MALAYSIA
```


Language: English (Malaysia)

### ENGLISH_NEW_ZEALAND {#ENGLISH-NEW-ZEALAND}
```
public static int ENGLISH_NEW_ZEALAND
```


Language: English (New Zealand)

### ENGLISH_PHILIPPINES {#ENGLISH-PHILIPPINES}
```
public static int ENGLISH_PHILIPPINES
```


Language: English (Philippines)

### ENGLISH_SINGAPORE {#ENGLISH-SINGAPORE}
```
public static int ENGLISH_SINGAPORE
```


Language: English (Singapore)

### ENGLISH_SOUTH_AFRICA {#ENGLISH-SOUTH-AFRICA}
```
public static int ENGLISH_SOUTH_AFRICA
```


Language: English (South Africa)

### ENGLISH_TRINIDAD_AND_TOBAGO {#ENGLISH-TRINIDAD-AND-TOBAGO}
```
public static int ENGLISH_TRINIDAD_AND_TOBAGO
```


Language: English (Trinidad and Tobago)

### ENGLISH_UK {#ENGLISH-UK}
```
public static int ENGLISH_UK
```


Language: English (UK)

### ENGLISH_US {#ENGLISH-US}
```
public static int ENGLISH_US
```


Language: English (US)

### ENGLISH_ZIMBABWE {#ENGLISH-ZIMBABWE}
```
public static int ENGLISH_ZIMBABWE
```


Language: English (Zimbabwe)

### ESTONIAN {#ESTONIAN}
```
public static int ESTONIAN
```


Language: Estonian

### FAEROESE {#FAEROESE}
```
public static int FAEROESE
```


Language: Faeroese

### FILIPINO {#FILIPINO}
```
public static int FILIPINO
```


Language: Filipino

### FINNISH {#FINNISH}
```
public static int FINNISH
```


Language: Finnish

### FRENCH_BELGIUM {#FRENCH-BELGIUM}
```
public static int FRENCH_BELGIUM
```


Language: French (Belgium)

### FRENCH_CANADA {#FRENCH-CANADA}
```
public static int FRENCH_CANADA
```


Language: French (Canada)

### FRENCH_FRANCE {#FRENCH-FRANCE}
```
public static int FRENCH_FRANCE
```


Language: French (France)

### FRENCH_LUXEMBOURG {#FRENCH-LUXEMBOURG}
```
public static int FRENCH_LUXEMBOURG
```


Language: French (Luxembourg)

### FRENCH_MONACO {#FRENCH-MONACO}
```
public static int FRENCH_MONACO
```


Language: French (Monaco)

### FRENCH_SWITZERLAND {#FRENCH-SWITZERLAND}
```
public static int FRENCH_SWITZERLAND
```


Language: French (Switzerland)

### FRISIAN {#FRISIAN}
```
public static int FRISIAN
```


Language: Frisian

### FULAH_LATIN_SENEGAL {#FULAH-LATIN-SENEGAL}
```
public static int FULAH_LATIN_SENEGAL
```


Language: Fulah (Latin, Senegal)

### FULAH_NIGERIA {#FULAH-NIGERIA}
```
public static int FULAH_NIGERIA
```


Language: Fulah (Nigeria)

### GALICIAN {#GALICIAN}
```
public static int GALICIAN
```


Language: Galician

### GEORGIAN {#GEORGIAN}
```
public static int GEORGIAN
```


Language: Georgian

### GERMAN_AUSTRIA {#GERMAN-AUSTRIA}
```
public static int GERMAN_AUSTRIA
```


Language: German (Austria)

### GERMAN_GERMANY {#GERMAN-GERMANY}
```
public static int GERMAN_GERMANY
```


Language: German (Germany)

### GERMAN_LIECHTENSTEIN {#GERMAN-LIECHTENSTEIN}
```
public static int GERMAN_LIECHTENSTEIN
```


Language: German (Liechtenstein)

### GERMAN_LUXEMBOURG {#GERMAN-LUXEMBOURG}
```
public static int GERMAN_LUXEMBOURG
```


Language: German (Luxembourg)

### GERMAN_SWITZERLAND {#GERMAN-SWITZERLAND}
```
public static int GERMAN_SWITZERLAND
```


Language: German (Switzerland)

### GREEK {#GREEK}
```
public static int GREEK
```


Language: Greek

### GREENLANDIC {#GREENLANDIC}
```
public static int GREENLANDIC
```


Language: Greenlandic

### GUARANI {#GUARANI}
```
public static int GUARANI
```


Language: Guarani

### GUJARATI {#GUJARATI}
```
public static int GUJARATI
```


Language: Gujarati

### HAUSA {#HAUSA}
```
public static int HAUSA
```


Language: Hausa

### HAWAIIAN {#HAWAIIAN}
```
public static int HAWAIIAN
```


Language: Hawaiian

### HEBREW {#HEBREW}
```
public static int HEBREW
```


Language: Hebrew

### HINDI {#HINDI}
```
public static int HINDI
```


Language: Hindi

### HUNGARIAN {#HUNGARIAN}
```
public static int HUNGARIAN
```


Language: Hungarian

### ICELANDIC {#ICELANDIC}
```
public static int ICELANDIC
```


Language: Icelandic

### IGBO {#IGBO}
```
public static int IGBO
```


Language: Igbo

### INARI_SAMI_FINLAND {#INARI-SAMI-FINLAND}
```
public static int INARI_SAMI_FINLAND
```


Language: Inari Sami (Finland)

### INDONESIAN {#INDONESIAN}
```
public static int INDONESIAN
```


Language: Indonesian

### INUKTITUT_LATIN {#INUKTITUT-LATIN}
```
public static int INUKTITUT_LATIN
```


Language: Inuktitut (Latin)

### INUKTITUT_SYLLABICS {#INUKTITUT-SYLLABICS}
```
public static int INUKTITUT_SYLLABICS
```


Language: Inuktitut (Syllabics)

### IRISH {#IRISH}
```
public static int IRISH
```


Language: Irish

### ISI_XHOSA {#ISI-XHOSA}
```
public static int ISI_XHOSA
```


Language: IsiXhosa

### ISI_ZULU {#ISI-ZULU}
```
public static int ISI_ZULU
```


Language: IsiZulu

### ITALIAN_ITALY {#ITALIAN-ITALY}
```
public static int ITALIAN_ITALY
```


Language: Italian (Italy)

### ITALIAN_SWITZERLAND {#ITALIAN-SWITZERLAND}
```
public static int ITALIAN_SWITZERLAND
```


Language: Italian (Switzerland)

### JAPANESE {#JAPANESE}
```
public static int JAPANESE
```


Language: Japanese

### KANNADA {#KANNADA}
```
public static int KANNADA
```


Language: Kannada

### KANURI {#KANURI}
```
public static int KANURI
```


Language: Kanuri

### KASHMIRI {#KASHMIRI}
```
public static int KASHMIRI
```


Language: Kashmiri

### KASHMIRI_ARABIC {#KASHMIRI-ARABIC}
```
public static int KASHMIRI_ARABIC
```


Language: Kashmiri (Arabic)

### KAZAKH {#KAZAKH}
```
public static int KAZAKH
```


Language: Kazakh

### KHMER {#KHMER}
```
public static int KHMER
```


Language: Khmer

### KICHE {#KICHE}
```
public static int KICHE
```


Language: Kiche

### KINYARWANDA {#KINYARWANDA}
```
public static int KINYARWANDA
```


Language: Kinyarwanda

### KISWAHILI {#KISWAHILI}
```
public static int KISWAHILI
```


Language: Kiswahili

### KONKANI {#KONKANI}
```
public static int KONKANI
```


Language: Konkani

### KOREAN {#KOREAN}
```
public static int KOREAN
```


Language: Korean

### KYRGYZ {#KYRGYZ}
```
public static int KYRGYZ
```


Language: Kyrgyz

### LAO {#LAO}
```
public static int LAO
```


Language: Lao

### LATIN {#LATIN}
```
public static int LATIN
```


Language: Latin

### LATVIAN {#LATVIAN}
```
public static int LATVIAN
```


Language: Latvian

### LITHUANIAN {#LITHUANIAN}
```
public static int LITHUANIAN
```


Language: Lithuanian

### LOWER_SORBIAN {#LOWER-SORBIAN}
```
public static int LOWER_SORBIAN
```


Language: Lower Sorbian

### LULE_SAMI_NORWAY {#LULE-SAMI-NORWAY}
```
public static int LULE_SAMI_NORWAY
```


Language: Lule Sami (Norway)

### LULE_SAMI_SWEDEN {#LULE-SAMI-SWEDEN}
```
public static int LULE_SAMI_SWEDEN
```


Language: Lule Sami (Sweden)

### LUXEMBOUGISH {#LUXEMBOUGISH}
```
public static int LUXEMBOUGISH
```


Language: Luxembourgish

### MACEDONIAN {#MACEDONIAN}
```
public static int MACEDONIAN
```


Language: Macedonian

### MALAYALAM {#MALAYALAM}
```
public static int MALAYALAM
```


Language: Malayalam

### MALAY_BRUNEI_DARUSSALAM {#MALAY-BRUNEI-DARUSSALAM}
```
public static int MALAY_BRUNEI_DARUSSALAM
```


Language: Malay (Brunei Darussalam)

### MALAY_MALAYSIA {#MALAY-MALAYSIA}
```
public static int MALAY_MALAYSIA
```


Language: Malay (Malaysia)

### MALTESE {#MALTESE}
```
public static int MALTESE
```


Language: Maltese

### MANIPURI {#MANIPURI}
```
public static int MANIPURI
```


Language: Manipuri

### MAORI {#MAORI}
```
public static int MAORI
```


Language: Maori

### MAPUDUNGUN_CHILE {#MAPUDUNGUN-CHILE}
```
public static int MAPUDUNGUN_CHILE
```


Language: Mapudungun (Chile)

### MARATHI {#MARATHI}
```
public static int MARATHI
```


Language: Marathi

### MOHAWK {#MOHAWK}
```
public static int MOHAWK
```


Language: Mohawk

### MONGOLIAN_CYRILLIC {#MONGOLIAN-CYRILLIC}
```
public static int MONGOLIAN_CYRILLIC
```


Language: Mongolian (Cyrillic)

### MONGOLIAN_MONGOLIAN {#MONGOLIAN-MONGOLIAN}
```
public static int MONGOLIAN_MONGOLIAN
```


Language: Mongolian (Mongolian)

### NEPALI {#NEPALI}
```
public static int NEPALI
```


Language: Nepali

### NORTHERN_SAMI_FINLAND {#NORTHERN-SAMI-FINLAND}
```
public static int NORTHERN_SAMI_FINLAND
```


Language: Northern Sami (Finland)

### NORTHERN_SAMI_NORWAY {#NORTHERN-SAMI-NORWAY}
```
public static int NORTHERN_SAMI_NORWAY
```


Language: Northern Sami (Norway)

### NORTHERN_SAMI_SWEDEN {#NORTHERN-SAMI-SWEDEN}
```
public static int NORTHERN_SAMI_SWEDEN
```


Language: Northern Sami (Sweden)

### NORWEGIAN_BOKMAL {#NORWEGIAN-BOKMAL}
```
public static int NORWEGIAN_BOKMAL
```


Language: Norwegian Bokmal

### NORWEGIAN_NYNORSK {#NORWEGIAN-NYNORSK}
```
public static int NORWEGIAN_NYNORSK
```


Language: Norwegian Nynorsk

### ORIYA {#ORIYA}
```
public static int ORIYA
```


Language: Oriya

### OROMO {#OROMO}
```
public static int OROMO
```


Language: Oromo

### PAPIAMENTU {#PAPIAMENTU}
```
public static int PAPIAMENTU
```


Language: Papiamentu

### PASHTO {#PASHTO}
```
public static int PASHTO
```


Language: Pashto

### PERSIAN {#PERSIAN}
```
public static int PERSIAN
```


Language: Persian

### POLISH {#POLISH}
```
public static int POLISH
```


Language: Polish

### PORTUGUESE_BRAZIL {#PORTUGUESE-BRAZIL}
```
public static int PORTUGUESE_BRAZIL
```


Language: Portuguese (Brazil)

### PORTUGUESE_PORTUGAL {#PORTUGUESE-PORTUGAL}
```
public static int PORTUGUESE_PORTUGAL
```


Language: Portuguese (Portugal)

### PUNJABI_INDIA {#PUNJABI-INDIA}
```
public static int PUNJABI_INDIA
```


Language: Punjabi (India)

### PUNJABI_PAKISTAN {#PUNJABI-PAKISTAN}
```
public static int PUNJABI_PAKISTAN
```


Language: Punjabi (Pakistan)

### QUECHUA_BOLIVIA {#QUECHUA-BOLIVIA}
```
public static int QUECHUA_BOLIVIA
```


Language: Quechua (Bolivia)

### QUECHUA_ECUADOR {#QUECHUA-ECUADOR}
```
public static int QUECHUA_ECUADOR
```


Language: Quechua (Ecuador)

### QUECHUA_PERU {#QUECHUA-PERU}
```
public static int QUECHUA_PERU
```


Language: Quechua (Peru)

### ROMANIAN {#ROMANIAN}
```
public static int ROMANIAN
```


Language: Romanian

### ROMANSH {#ROMANSH}
```
public static int ROMANSH
```


Language: Romansh

### RUSSIAN {#RUSSIAN}
```
public static int RUSSIAN
```


Language: Russian

### SAKHA {#SAKHA}
```
public static int SAKHA
```


Language: Sakha

### SANSKRIT {#SANSKRIT}
```
public static int SANSKRIT
```


Language: Sanskrit

### SCOTTISH_GAELIC {#SCOTTISH-GAELIC}
```
public static int SCOTTISH_GAELIC
```


Language: Scottish Gaelic

### SERBIAN_CYRILLIC_BOSNIA_AND_HERZEGOVINA {#SERBIAN-CYRILLIC-BOSNIA-AND-HERZEGOVINA}
```
public static int SERBIAN_CYRILLIC_BOSNIA_AND_HERZEGOVINA
```


Language: Serbian (Cyrillic, Bosnia and Herzegovina)

### SERBIAN_CYRILLIC_SERBIA_AND_MONTENEGRO {#SERBIAN-CYRILLIC-SERBIA-AND-MONTENEGRO}
```
public static int SERBIAN_CYRILLIC_SERBIA_AND_MONTENEGRO
```


Language: Serbian (Cyrillic, Serbia and Montenegro)

### SERBIAN_LATIN_BOSNIA_AND_HERZEGOVINA {#SERBIAN-LATIN-BOSNIA-AND-HERZEGOVINA}
```
public static int SERBIAN_LATIN_BOSNIA_AND_HERZEGOVINA
```


Language: Serbian (Latin, Bosnia and Herzegovina)

### SERBIAN_LATIN_SERBIA_AND_MONTENEGRO {#SERBIAN-LATIN-SERBIA-AND-MONTENEGRO}
```
public static int SERBIAN_LATIN_SERBIA_AND_MONTENEGRO
```


Language: Serbian (Latin, Serbia and Montenegro)

### SINDHI {#SINDHI}
```
public static int SINDHI
```


Language: Sindhi

### SINDHI_DEVANAGARIC {#SINDHI-DEVANAGARIC}
```
public static int SINDHI_DEVANAGARIC
```


Language: Sindhi (Devanagari)

### SINHALESE {#SINHALESE}
```
public static int SINHALESE
```


Language: Sinhalese

### SLOVAK {#SLOVAK}
```
public static int SLOVAK
```


Language: Slovak

### SLOVENIAN {#SLOVENIAN}
```
public static int SLOVENIAN
```


Language: Slovenian

### SOMALI {#SOMALI}
```
public static int SOMALI
```


Language: Somali

### SORBIAN {#SORBIAN}
```
public static int SORBIAN
```


Language: Sorbian

### SPANISH_ARGENTINA {#SPANISH-ARGENTINA}
```
public static int SPANISH_ARGENTINA
```


Language: Spanish (Argentina)

### SPANISH_BOLIVIA {#SPANISH-BOLIVIA}
```
public static int SPANISH_BOLIVIA
```


Language: Spanish (Bolivia)

### SPANISH_CHILE {#SPANISH-CHILE}
```
public static int SPANISH_CHILE
```


Language: Spanish (Chile)

### SPANISH_COLOMBIA {#SPANISH-COLOMBIA}
```
public static int SPANISH_COLOMBIA
```


Language: Spanish (Colombia)

### SPANISH_COSTA_RICA {#SPANISH-COSTA-RICA}
```
public static int SPANISH_COSTA_RICA
```


Language: Spanish (Costa Rica)

### SPANISH_DOMINICAN_REPUBLIC {#SPANISH-DOMINICAN-REPUBLIC}
```
public static int SPANISH_DOMINICAN_REPUBLIC
```


Language: Spanish (Dominican Republic)

### SPANISH_ECUADOR {#SPANISH-ECUADOR}
```
public static int SPANISH_ECUADOR
```


Language: Spanish (Ecuador)

### SPANISH_EL_SALVADOR {#SPANISH-EL-SALVADOR}
```
public static int SPANISH_EL_SALVADOR
```


Language: Spanish (El Salvador)

### SPANISH_GUATEMALA {#SPANISH-GUATEMALA}
```
public static int SPANISH_GUATEMALA
```


Language: Spanish (Guatemala)

### SPANISH_HONDURAS {#SPANISH-HONDURAS}
```
public static int SPANISH_HONDURAS
```


Language: Spanish (Honduras)

### SPANISH_MEXICO {#SPANISH-MEXICO}
```
public static int SPANISH_MEXICO
```


Language: Spanish (Mexico)

### SPANISH_NICARAGUA {#SPANISH-NICARAGUA}
```
public static int SPANISH_NICARAGUA
```


Language: Spanish (Nicaragua)

### SPANISH_PANAMA {#SPANISH-PANAMA}
```
public static int SPANISH_PANAMA
```


Language: Spanish (Panama)

### SPANISH_PARAGUAY {#SPANISH-PARAGUAY}
```
public static int SPANISH_PARAGUAY
```


Language: Spanish (Paraguay)

### SPANISH_PERU {#SPANISH-PERU}
```
public static int SPANISH_PERU
```


Language: Spanish (Peru)

### SPANISH_PUERTO_RICO {#SPANISH-PUERTO-RICO}
```
public static int SPANISH_PUERTO_RICO
```


Language: Spanish (Puerto Rico)

### SPANISH_SPAIN_MODERN_SORT {#SPANISH-SPAIN-MODERN-SORT}
```
public static int SPANISH_SPAIN_MODERN_SORT
```


Language: Spanish (Spain, Modern Sort)

### SPANISH_SPAIN_TRADITIONAL_SORT {#SPANISH-SPAIN-TRADITIONAL-SORT}
```
public static int SPANISH_SPAIN_TRADITIONAL_SORT
```


Language: Spanish (Spain, Traditional Sort)

### SPANISH_URUGUAY {#SPANISH-URUGUAY}
```
public static int SPANISH_URUGUAY
```


Language: Spanish (Uruguay)

### SPANISH_VENEZUELA {#SPANISH-VENEZUELA}
```
public static int SPANISH_VENEZUELA
```


Language: Spanish (Venezuela)

### SUTU {#SUTU}
```
public static int SUTU
```


Language: Sutu

### SWEDISH_FINLAND {#SWEDISH-FINLAND}
```
public static int SWEDISH_FINLAND
```


Language: Swedish (Finland)

### SWEDISH_SWEDEN {#SWEDISH-SWEDEN}
```
public static int SWEDISH_SWEDEN
```


Language: Swedish (Sweden)

### SYRIAC {#SYRIAC}
```
public static int SYRIAC
```


Language: Syriac

### TAJIK {#TAJIK}
```
public static int TAJIK
```


Language: Tajik

### TAMAZIGHT {#TAMAZIGHT}
```
public static int TAMAZIGHT
```


Language: Tamazight

### TAMAZIGHT_LATIN {#TAMAZIGHT-LATIN}
```
public static int TAMAZIGHT_LATIN
```


Language: Tamazight (Latin)

### TAMIL {#TAMIL}
```
public static int TAMIL
```


Language: Tamil

### TATAR {#TATAR}
```
public static int TATAR
```


Language: Tatar

### TELUGU {#TELUGU}
```
public static int TELUGU
```


Language: Telugu

### THAI {#THAI}
```
public static int THAI
```


Language: Thai

### TIBETAN_BUTAN {#TIBETAN-BUTAN}
```
public static int TIBETAN_BUTAN
```


Language: Tibetan (Bhutan)

### TIBETAN_CHINA {#TIBETAN-CHINA}
```
public static int TIBETAN_CHINA
```


Language: Tibetan (China)

### TIGRIGNA_ERITREA {#TIGRIGNA-ERITREA}
```
public static int TIGRIGNA_ERITREA
```


Language: Tigrigna (Eritrea)

### TIGRIGNA_ETHIOPIA {#TIGRIGNA-ETHIOPIA}
```
public static int TIGRIGNA_ETHIOPIA
```


Language: Tigrigna (Ethiopia)

### TSONGA {#TSONGA}
```
public static int TSONGA
```


Language: Tsonga

### TSWANA {#TSWANA}
```
public static int TSWANA
```


Language: Tswana

### TURKISH {#TURKISH}
```
public static int TURKISH
```


Language: Turkish

### TURKMEN {#TURKMEN}
```
public static int TURKMEN
```


Language: Turkmen

### UKRAINIAN {#UKRAINIAN}
```
public static int UKRAINIAN
```


Language: Ukrainian

### URDU {#URDU}
```
public static int URDU
```


Language: Urdu

### UZBEK_CYRILLIC {#UZBEK-CYRILLIC}
```
public static int UZBEK_CYRILLIC
```


Language: Uzbek (Cyrillic)

### UZBEK_LATIN {#UZBEK-LATIN}
```
public static int UZBEK_LATIN
```


Language: Uzbek (Latin)

### VENDA {#VENDA}
```
public static int VENDA
```


Language: Venda

### VIETNAMESE {#VIETNAMESE}
```
public static int VIETNAMESE
```


Language: Vietnamese

### WELSH {#WELSH}
```
public static int WELSH
```


Language: Welsh

### YI {#YI}
```
public static int YI
```


Language: Yi

### YIDDISH {#YIDDISH}
```
public static int YIDDISH
```


Language: Yiddish

### YORUBA {#YORUBA}
```
public static int YORUBA
```


Language: Yoruba

### length {#length}
```
public static int length
```


### fromName(String editingLanguageName) {#fromName-java.lang.String}
```
public static int fromName(String editingLanguageName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| editingLanguageName | java.lang.String |  |

**Returns:**
int
### getName(int editingLanguage) {#getName-int}
```
public static String getName(int editingLanguage)
```




**Parameters:**
| Parameter | Type | Description |
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
| Parameter | Type | Description |
| --- | --- | --- |
| editingLanguage | int |  |

**Returns:**
java.lang.String
