---
title: "EditingLanguage"
linktitle: "EditingLanguage"
second_title: "Aspose.Words für Java"
description: "Gibt die Bearbeitungssprache in Java an."
type: docs
weight: 182
url: /de/java/com.aspose.words/editinglanguage/
---

**Inheritance:**
java.lang.Object
```
public class EditingLanguage
```

Gibt die Bearbeitungssprache an.

 **Examples:** 

Zeigt, wie man Sprachpräferenzen beim Laden eines Dokuments anwendet.

```

 LoadOptions loadOptions = new LoadOptions();
 loadOptions.getLanguagePreferences().addEditingLanguage(EditingLanguage.JAPANESE);

 Document doc = new Document(getMyDir() + "No default editing language.docx", loadOptions);

 int localeIdFarEast = doc.getStyles().getDefaultFont().getLocaleIdFarEast();
 System.out.println(localeIdFarEast == EditingLanguage.JAPANESE
         ? "The document either has no any FarEast language set in defaults or it was set to Japanese originally."
         : "The document default FarEast language was set to another than Japanese language originally, so it is not overridden.");
 
```
## Felder

| Feld | Beschreibung |
| --- | --- |
| [AFRIKAANS](#AFRIKAANS) | Sprache: Afrikaans |
| [ALBANIAN](#ALBANIAN) | Sprache: Albanisch |
| [ALSATIAN](#ALSATIAN) | Sprache: Elsässisch |
| [AMHARIC](#AMHARIC) | Sprache: Amharisch |
| [ARABIC_ALGERIA](#ARABIC-ALGERIA) | Sprache: Arabisch (Algerien) |
| [ARABIC_BAHRAIN](#ARABIC-BAHRAIN) | Sprache: Arabisch (Bahrain) |
| [ARABIC_EGYPT](#ARABIC-EGYPT) | Sprache: Arabisch (Ägypten) |
| [ARABIC_IRAQ](#ARABIC-IRAQ) | Sprache: Arabisch (Irak) |
| [ARABIC_JORDAN](#ARABIC-JORDAN) | Sprache: Arabisch (Jordanien) |
| [ARABIC_KUWAIT](#ARABIC-KUWAIT) | Sprache: Arabisch (Kuwait) |
| [ARABIC_LEBANON](#ARABIC-LEBANON) | Sprache: Arabisch (Libanon) |
| [ARABIC_LIBYA](#ARABIC-LIBYA) | Sprache: Arabisch (Libyen) |
| [ARABIC_MOROCCO](#ARABIC-MOROCCO) | Sprache: Arabisch (Marokko) |
| [ARABIC_OMAN](#ARABIC-OMAN) | Sprache: Arabisch (Oman) |
| [ARABIC_QATAR](#ARABIC-QATAR) | Sprache: Arabisch (Katar) |
| [ARABIC_SAUDI_ARABIA](#ARABIC-SAUDI-ARABIA) | Sprache: Arabisch (Saudi-Arabien) |
| [ARABIC_SYRIA](#ARABIC-SYRIA) | Sprache: Arabisch (Syrien) |
| [ARABIC_TUNISIA](#ARABIC-TUNISIA) | Sprache: Arabisch (Tunesien) |
| [ARABIC_UAE](#ARABIC-UAE) | Sprache: Arabisch (Vereinigte Arabische Emirate) |
| [ARABIC_YEMEN](#ARABIC-YEMEN) | Sprache: Arabisch (Jemen) |
| [ARMENIAN](#ARMENIAN) | Sprache: Armenisch |
| [ASSAMESE](#ASSAMESE) | Sprache: Assamesisch |
| [AZERBAIJANI_CYRILLIC](#AZERBAIJANI-CYRILLIC) | Sprache: Aserbaidschanisch (Kyrillisch) |
| [AZERBAIJANI_LATIN](#AZERBAIJANI-LATIN) | Sprache: Aserbaidschanisch (Lateinisch) |
| [BANGLA_BANGLADESH](#BANGLA-BANGLADESH) | Sprache: Bangla (Bangladesch) |
| [BANGLA_INDIA](#BANGLA-INDIA) | Sprache: Bangla (Indien) |
| [BASHKIR](#BASHKIR) | Sprache: Baschkirisch |
| [BASQUE](#BASQUE) | Sprache: Baskisch |
| [BELARUSIAN](#BELARUSIAN) | Sprache: Weißrussisch |
| [BOSNIAN_CYRILLIC](#BOSNIAN-CYRILLIC) | Sprache: Bosnisch (Kyrillisch) |
| [BOSNIAN_LATIN](#BOSNIAN-LATIN) | Sprache: Bosnisch (Lateinisch) |
| [BRETON](#BRETON) | Sprache: Bretonisch |
| [BULGARIAN](#BULGARIAN) | Sprache: Bulgarisch |
| [BURMESE](#BURMESE) | Sprache: Birmanisch |
| [CATALAN](#CATALAN) | Sprache: Katalanisch |
| [CENTRAL_KURDISH_IRAQ](#CENTRAL-KURDISH-IRAQ) | Sprache: Zentral-Kurdisch (Irak) |
| [CHEROKEE](#CHEROKEE) | Sprache: Cherokee |
| [CHINESE_HONG_KONG](#CHINESE-HONG-KONG) | Sprache: Chinesisch (Hongkong) |
| [CHINESE_MACAO](#CHINESE-MACAO) | Sprache: Chinesisch (Macao) |
| [CHINESE_PRC](#CHINESE-PRC) | Sprache: Chinesisch (VR China) |
| [CHINESE_SINGAPORE](#CHINESE-SINGAPORE) | Sprache: Chinesisch (Singapur) |
| [CHINESE_TAIWAN](#CHINESE-TAIWAN) | Sprache: Chinesisch (Taiwan) |
| [CORSICAN](#CORSICAN) | Sprache: Korsisch |
| [CROATIAN](#CROATIAN) | Sprache: Kroatisch |
| [CROATIAN_BOZNIA_AND_HERZEGOVINA](#CROATIAN-BOZNIA-AND-HERZEGOVINA) | Sprache: Kroatisch (Bosnien und Herzegowina) |
| [CZECH](#CZECH) | Sprache: Tschechisch |
| [DANISH](#DANISH) | Sprache: Dänisch |
| [DIVEHI](#DIVEHI) | Sprache: Divehi |
| [DUTCH_BELGIUM](#DUTCH-BELGIUM) | Sprache: Niederländisch (Belgien) |
| [DUTCH_NETHERLANDS](#DUTCH-NETHERLANDS) | Sprache: Niederländisch (Niederlande) |
| [EDO](#EDO) | Sprache: Edo |
| [ENGLISH_AUSTRALIA](#ENGLISH-AUSTRALIA) | Sprache: Englisch (Australien) |
| [ENGLISH_BELIZE](#ENGLISH-BELIZE) | Sprache: Englisch (Belize) |
| [ENGLISH_CANADA](#ENGLISH-CANADA) | Sprache: Englisch (Kanada) |
| [ENGLISH_CARIBBEAN](#ENGLISH-CARIBBEAN) | Sprache: Englisch (Karibik) |
| [ENGLISH_HONG_KONG](#ENGLISH-HONG-KONG) | Sprache: Englisch (Hongkong) |
| [ENGLISH_INDIA](#ENGLISH-INDIA) | Sprache: Englisch (Indien) |
| [ENGLISH_INDONESIA](#ENGLISH-INDONESIA) | Sprache: Englisch (Indonesien) |
| [ENGLISH_IRELAND](#ENGLISH-IRELAND) | Sprache: Englisch (Irland) |
| [ENGLISH_JAMAICA](#ENGLISH-JAMAICA) | Sprache: Englisch (Jamaika) |
| [ENGLISH_MALAYSIA](#ENGLISH-MALAYSIA) | Sprache: Englisch (Malaysia) |
| [ENGLISH_NEW_ZEALAND](#ENGLISH-NEW-ZEALAND) | Sprache: Englisch (Neuseeland) |
| [ENGLISH_PHILIPPINES](#ENGLISH-PHILIPPINES) | Sprache: Englisch (Philippinen) |
| [ENGLISH_SINGAPORE](#ENGLISH-SINGAPORE) | Sprache: Englisch (Singapur) |
| [ENGLISH_SOUTH_AFRICA](#ENGLISH-SOUTH-AFRICA) | Sprache: Englisch (Südafrika) |
| [ENGLISH_TRINIDAD_AND_TOBAGO](#ENGLISH-TRINIDAD-AND-TOBAGO) | Sprache: Englisch (Trinidad und Tobago) |
| [ENGLISH_UK](#ENGLISH-UK) | Sprache: Englisch (Vereinigtes Königreich) |
| [ENGLISH_US](#ENGLISH-US) | Sprache: Englisch (USA) |
| [ENGLISH_ZIMBABWE](#ENGLISH-ZIMBABWE) | Sprache: Englisch (Simbabwe) |
| [ESTONIAN](#ESTONIAN) | Sprache: Estnisch |
| [FAEROESE](#FAEROESE) | Sprache: Färöisch |
| [FILIPINO](#FILIPINO) | Sprache: Filipino |
| [FINNISH](#FINNISH) | Sprache: Finnisch |
| [FRENCH_BELGIUM](#FRENCH-BELGIUM) | Sprache: Französisch (Belgien) |
| [FRENCH_CANADA](#FRENCH-CANADA) | Sprache: Französisch (Kanada) |
| [FRENCH_FRANCE](#FRENCH-FRANCE) | Sprache: Französisch (Frankreich) |
| [FRENCH_LUXEMBOURG](#FRENCH-LUXEMBOURG) | Sprache: Französisch (Luxemburg) |
| [FRENCH_MONACO](#FRENCH-MONACO) | Sprache: Französisch (Monaco) |
| [FRENCH_SWITZERLAND](#FRENCH-SWITZERLAND) | Sprache: Französisch (Schweiz) |
| [FRISIAN](#FRISIAN) | Sprache: Friesisch |
| [FULAH_LATIN_SENEGAL](#FULAH-LATIN-SENEGAL) | Sprache: Fulah (Latein, Senegal) |
| [FULAH_NIGERIA](#FULAH-NIGERIA) | Sprache: Fulah (Nigeria) |
| [GALICIAN](#GALICIAN) | Sprache: Galicisch |
| [GEORGIAN](#GEORGIAN) | Sprache: Georgisch |
| [GERMAN_AUSTRIA](#GERMAN-AUSTRIA) | Sprache: Deutsch (Österreich) |
| [GERMAN_GERMANY](#GERMAN-GERMANY) | Sprache: Deutsch (Deutschland) |
| [GERMAN_LIECHTENSTEIN](#GERMAN-LIECHTENSTEIN) | Sprache: Deutsch (Liechtenstein) |
| [GERMAN_LUXEMBOURG](#GERMAN-LUXEMBOURG) | Sprache: Deutsch (Luxemburg) |
| [GERMAN_SWITZERLAND](#GERMAN-SWITZERLAND) | Sprache: Deutsch (Schweiz) |
| [GREEK](#GREEK) | Sprache: Griechisch |
| [GREENLANDIC](#GREENLANDIC) | Sprache: Grönländisch |
| [GUARANI](#GUARANI) | Sprache: Guaraní |
| [GUJARATI](#GUJARATI) | Sprache: Gujarati |
| [HAUSA](#HAUSA) | Sprache: Hausa |
| [HAWAIIAN](#HAWAIIAN) | Sprache: Hawaiisch |
| [HEBREW](#HEBREW) | Sprache: Hebräisch |
| [HINDI](#HINDI) | Sprache: Hindi |
| [HUNGARIAN](#HUNGARIAN) | Sprache: Ungarisch |
| [ICELANDIC](#ICELANDIC) | Sprache: Isländisch |
| [IGBO](#IGBO) | Sprache: Igbo |
| [INARI_SAMI_FINLAND](#INARI-SAMI-FINLAND) | Sprache: Inari-Samisch (Finnland) |
| [INDONESIAN](#INDONESIAN) | Sprache: Indonesisch |
| [INUKTITUT_LATIN](#INUKTITUT-LATIN) | Sprache: Inuktitut (Latein) |
| [INUKTITUT_SYLLABICS](#INUKTITUT-SYLLABICS) | Sprache: Inuktitut (Silben) |
| [IRISH](#IRISH) | Sprache: Irisch |
| [ISI_XHOSA](#ISI-XHOSA) | Sprache: IsiXhosa |
| [ISI_ZULU](#ISI-ZULU) | Sprache: IsiZulu |
| [ITALIAN_ITALY](#ITALIAN-ITALY) | Sprache: Italienisch (Italien) |
| [ITALIAN_SWITZERLAND](#ITALIAN-SWITZERLAND) | Sprache: Italienisch (Schweiz) |
| [JAPANESE](#JAPANESE) | Sprache: Japanisch |
| [KANNADA](#KANNADA) | Sprache: Kannada |
| [KANURI](#KANURI) | Sprache: Kanuri |
| [KASHMIRI](#KASHMIRI) | Sprache: Kaschmiri |
| [KASHMIRI_ARABIC](#KASHMIRI-ARABIC) | Sprache: Kaschmiri (Arabisch) |
| [KAZAKH](#KAZAKH) | Sprache: Kasachisch |
| [KHMER](#KHMER) | Sprache: Khmer |
| [KICHE](#KICHE) | Sprache: Kiche |
| [KINYARWANDA](#KINYARWANDA) | Sprache: Kinyarwanda |
| [KISWAHILI](#KISWAHILI) | Sprache: Swahili |
| [KONKANI](#KONKANI) | Sprache: Konkani |
| [KOREAN](#KOREAN) | Sprache: Koreanisch |
| [KYRGYZ](#KYRGYZ) | Sprache: Kirgisisch |
| [LAO](#LAO) | Sprache: Laotisch |
| [LATIN](#LATIN) | Sprache: Latein |
| [LATVIAN](#LATVIAN) | Sprache: Lettisch |
| [LITHUANIAN](#LITHUANIAN) | Sprache: Litauisch |
| [LOWER_SORBIAN](#LOWER-SORBIAN) | Sprache: Niedersorbisch |
| [LULE_SAMI_NORWAY](#LULE-SAMI-NORWAY) | Sprache: Lule-Sami (Norwegen) |
| [LULE_SAMI_SWEDEN](#LULE-SAMI-SWEDEN) | Sprache: Lule-Sami (Schweden) |
| [LUXEMBOUGISH](#LUXEMBOUGISH) | Sprache: Luxemburgisch |
| [MACEDONIAN](#MACEDONIAN) | Sprache: Mazedonisch |
| [MALAYALAM](#MALAYALAM) | Sprache: Malayalam |
| [MALAY_BRUNEI_DARUSSALAM](#MALAY-BRUNEI-DARUSSALAM) | Sprache: Malaiisch (Brunei Darussalam) |
| [MALAY_MALAYSIA](#MALAY-MALAYSIA) | Sprache: Malaiisch (Malaysia) |
| [MALTESE](#MALTESE) | Sprache: Maltesisch |
| [MANIPURI](#MANIPURI) | Sprache: Manipuri |
| [MAORI](#MAORI) | Sprache: Maori |
| [MAPUDUNGUN_CHILE](#MAPUDUNGUN-CHILE) | Sprache: Mapudungun (Chile) |
| [MARATHI](#MARATHI) | Sprache: Marathi |
| [MOHAWK](#MOHAWK) | Sprache: Mohawk |
| [MONGOLIAN_CYRILLIC](#MONGOLIAN-CYRILLIC) | Sprache: Mongolisch (Kyrillisch) |
| [MONGOLIAN_MONGOLIAN](#MONGOLIAN-MONGOLIAN) | Sprache: Mongolisch (Mongolisch) |
| [NEPALI](#NEPALI) | Sprache: Nepali |
| [NORTHERN_SAMI_FINLAND](#NORTHERN-SAMI-FINLAND) | Sprache: Nordsamisch (Finnland) |
| [NORTHERN_SAMI_NORWAY](#NORTHERN-SAMI-NORWAY) | Sprache: Nordsamisch (Norwegen) |
| [NORTHERN_SAMI_SWEDEN](#NORTHERN-SAMI-SWEDEN) | Sprache: Nordsamisch (Schweden) |
| [NORWEGIAN_BOKMAL](#NORWEGIAN-BOKMAL) | Sprache: Norwegisch Bokmål |
| [NORWEGIAN_NYNORSK](#NORWEGIAN-NYNORSK) | Sprache: Norwegisch Nynorsk |
| [ORIYA](#ORIYA) | Sprache: Oriya |
| [OROMO](#OROMO) | Sprache: Oromo |
| [PAPIAMENTU](#PAPIAMENTU) | Sprache: Papiamentu |
| [PASHTO](#PASHTO) | Sprache: Paschtunisch |
| [PERSIAN](#PERSIAN) | Sprache: Persisch |
| [POLISH](#POLISH) | Sprache: Polnisch |
| [PORTUGUESE_BRAZIL](#PORTUGUESE-BRAZIL) | Sprache: Portugiesisch (Brasilien) |
| [PORTUGUESE_PORTUGAL](#PORTUGUESE-PORTUGAL) | Sprache: Portugiesisch (Portugal) |
| [PUNJABI_INDIA](#PUNJABI-INDIA) | Sprache: Punjabi (Indien) |
| [PUNJABI_PAKISTAN](#PUNJABI-PAKISTAN) | Sprache: Punjabi (Pakistan) |
| [QUECHUA_BOLIVIA](#QUECHUA-BOLIVIA) | Sprache: Quechua (Bolivien) |
| [QUECHUA_ECUADOR](#QUECHUA-ECUADOR) | Sprache: Quechua (Ecuador) |
| [QUECHUA_PERU](#QUECHUA-PERU) | Sprache: Quechua (Peru) |
| [ROMANIAN](#ROMANIAN) | Sprache: Rumänisch |
| [ROMANSH](#ROMANSH) | Sprache: Rätoromanisch |
| [RUSSIAN](#RUSSIAN) | Sprache: Russisch |
| [SAKHA](#SAKHA) | Sprache: Sakha |
| [SANSKRIT](#SANSKRIT) | Sprache: Sanskrit |
| [SCOTTISH_GAELIC](#SCOTTISH-GAELIC) | Sprache: Schottisch‑Gälisch |
| [SERBIAN_CYRILLIC_BOSNIA_AND_HERZEGOVINA](#SERBIAN-CYRILLIC-BOSNIA-AND-HERZEGOVINA) | Sprache: Serbisch (Kyrillisch, Bosnien und Herzegowina) |
| [SERBIAN_CYRILLIC_SERBIA_AND_MONTENEGRO](#SERBIAN-CYRILLIC-SERBIA-AND-MONTENEGRO) | Sprache: Serbisch (Kyrillisch, Serbien und Montenegro) |
| [SERBIAN_LATIN_BOSNIA_AND_HERZEGOVINA](#SERBIAN-LATIN-BOSNIA-AND-HERZEGOVINA) | Sprache: Serbisch (Lateinisch, Bosnien und Herzegowina) |
| [SERBIAN_LATIN_SERBIA_AND_MONTENEGRO](#SERBIAN-LATIN-SERBIA-AND-MONTENEGRO) | Sprache: Serbisch (Lateinisch, Serbien und Montenegro) |
| [SINDHI](#SINDHI) | Sprache: Sindhi |
| [SINDHI_DEVANAGARIC](#SINDHI-DEVANAGARIC) | Sprache: Sindhi (Devanagari) |
| [SINHALESE](#SINHALESE) | Sprache: Singhalesisch |
| [SLOVAK](#SLOVAK) | Sprache: Slowakisch |
| [SLOVENIAN](#SLOVENIAN) | Sprache: Slowenisch |
| [SOMALI](#SOMALI) | Sprache: Somali |
| [SORBIAN](#SORBIAN) | Sprache: Sorbisch |
| [SPANISH_ARGENTINA](#SPANISH-ARGENTINA) | Sprache: Spanisch (Argentinien) |
| [SPANISH_BOLIVIA](#SPANISH-BOLIVIA) | Sprache: Spanisch (Bolivien) |
| [SPANISH_CHILE](#SPANISH-CHILE) | Sprache: Spanisch (Chile) |
| [SPANISH_COLOMBIA](#SPANISH-COLOMBIA) | Sprache: Spanisch (Kolumbien) |
| [SPANISH_COSTA_RICA](#SPANISH-COSTA-RICA) | Sprache: Spanisch (Costa Rica) |
| [SPANISH_DOMINICAN_REPUBLIC](#SPANISH-DOMINICAN-REPUBLIC) | Sprache: Spanisch (Dominikanische Republik) |
| [SPANISH_ECUADOR](#SPANISH-ECUADOR) | Sprache: Spanisch (Ecuador) |
| [SPANISH_EL_SALVADOR](#SPANISH-EL-SALVADOR) | Sprache: Spanisch (El Salvador) |
| [SPANISH_GUATEMALA](#SPANISH-GUATEMALA) | Sprache: Spanisch (Guatemala) |
| [SPANISH_HONDURAS](#SPANISH-HONDURAS) | Sprache: Spanisch (Honduras) |
| [SPANISH_MEXICO](#SPANISH-MEXICO) | Sprache: Spanisch (Mexiko) |
| [SPANISH_NICARAGUA](#SPANISH-NICARAGUA) | Sprache: Spanisch (Nicaragua) |
| [SPANISH_PANAMA](#SPANISH-PANAMA) | Sprache: Spanisch (Panama) |
| [SPANISH_PARAGUAY](#SPANISH-PARAGUAY) | Sprache: Spanisch (Paraguay) |
| [SPANISH_PERU](#SPANISH-PERU) | Sprache: Spanisch (Peru) |
| [SPANISH_PUERTO_RICO](#SPANISH-PUERTO-RICO) | Sprache: Spanisch (Puerto Rico) |
| [SPANISH_SPAIN_MODERN_SORT](#SPANISH-SPAIN-MODERN-SORT) | Sprache: Spanisch (Spanien, Moderne Sortierung) |
| [SPANISH_SPAIN_TRADITIONAL_SORT](#SPANISH-SPAIN-TRADITIONAL-SORT) | Sprache: Spanisch (Spanien, Traditionelle Sortierung) |
| [SPANISH_URUGUAY](#SPANISH-URUGUAY) | Sprache: Spanisch (Uruguay) |
| [SPANISH_VENEZUELA](#SPANISH-VENEZUELA) | Sprache: Spanisch (Venezuela) |
| [SUTU](#SUTU) | Sprache: Sutu |
| [SWEDISH_FINLAND](#SWEDISH-FINLAND) | Sprache: Schwedisch (Finnland) |
| [SWEDISH_SWEDEN](#SWEDISH-SWEDEN) | Sprache: Schwedisch (Schweden) |
| [SYRIAC](#SYRIAC) | Sprache: Syrisch |
| [TAJIK](#TAJIK) | Sprache: Tadschikisch |
| [TAMAZIGHT](#TAMAZIGHT) | Sprache: Tamazight |
| [TAMAZIGHT_LATIN](#TAMAZIGHT-LATIN) | Sprache: Tamazight (Latein) |
| [TAMIL](#TAMIL) | Sprache: Tamil |
| [TATAR](#TATAR) | Sprache: Tatarisch |
| [TELUGU](#TELUGU) | Sprache: Telugu |
| [THAI](#THAI) | Sprache: Thai |
| [TIBETAN_BUTAN](#TIBETAN-BUTAN) | Sprache: Tibetisch (Bhutan) |
| [TIBETAN_CHINA](#TIBETAN-CHINA) | Sprache: Tibetisch (China) |
| [TIGRIGNA_ERITREA](#TIGRIGNA-ERITREA) | Sprache: Tigrinya (Eritrea) |
| [TIGRIGNA_ETHIOPIA](#TIGRIGNA-ETHIOPIA) | Sprache: Tigrinya (Äthiopien) |
| [TSONGA](#TSONGA) | Sprache: Tsonga |
| [TSWANA](#TSWANA) | Sprache: Tswana |
| [TURKISH](#TURKISH) | Sprache: Türkisch |
| [TURKMEN](#TURKMEN) | Sprache: Turkmenisch |
| [UKRAINIAN](#UKRAINIAN) | Sprache: Ukrainisch |
| [URDU](#URDU) | Sprache: Urdu |
| [UZBEK_CYRILLIC](#UZBEK-CYRILLIC) | Sprache: Usbekisch (Kyrillisch) |
| [UZBEK_LATIN](#UZBEK-LATIN) | Sprache: Usbekisch (Lateinisch) |
| [VENDA](#VENDA) | Sprache: Venda |
| [VIETNAMESE](#VIETNAMESE) | Sprache: Vietnamesisch |
| [WELSH](#WELSH) | Sprache: Walisisch |
| [YI](#YI) | Sprache: Yi |
| [YIDDISH](#YIDDISH) | Sprache: Jiddisch |
| [YORUBA](#YORUBA) | Sprache: Yoruba |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String editingLanguageName)](#fromName-java.lang.String) |  |
| [getName(int editingLanguage)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int editingLanguage)](#toString-int) |  |
### AFRIKAANS {#AFRIKAANS}
```
public static int AFRIKAANS
```


Sprache: Afrikaans

### ALBANIAN {#ALBANIAN}
```
public static int ALBANIAN
```


Sprache: Albanisch

### ALSATIAN {#ALSATIAN}
```
public static int ALSATIAN
```


Sprache: Elsässisch

### AMHARIC {#AMHARIC}
```
public static int AMHARIC
```


Sprache: Amharisch

### ARABIC_ALGERIA {#ARABIC-ALGERIA}
```
public static int ARABIC_ALGERIA
```


Sprache: Arabisch (Algerien)

### ARABIC_BAHRAIN {#ARABIC-BAHRAIN}
```
public static int ARABIC_BAHRAIN
```


Sprache: Arabisch (Bahrain)

### ARABIC_EGYPT {#ARABIC-EGYPT}
```
public static int ARABIC_EGYPT
```


Sprache: Arabisch (Ägypten)

### ARABIC_IRAQ {#ARABIC-IRAQ}
```
public static int ARABIC_IRAQ
```


Sprache: Arabisch (Irak)

### ARABIC_JORDAN {#ARABIC-JORDAN}
```
public static int ARABIC_JORDAN
```


Sprache: Arabisch (Jordanien)

### ARABIC_KUWAIT {#ARABIC-KUWAIT}
```
public static int ARABIC_KUWAIT
```


Sprache: Arabisch (Kuwait)

### ARABIC_LEBANON {#ARABIC-LEBANON}
```
public static int ARABIC_LEBANON
```


Sprache: Arabisch (Libanon)

### ARABIC_LIBYA {#ARABIC-LIBYA}
```
public static int ARABIC_LIBYA
```


Sprache: Arabisch (Libyen)

### ARABIC_MOROCCO {#ARABIC-MOROCCO}
```
public static int ARABIC_MOROCCO
```


Sprache: Arabisch (Marokko)

### ARABIC_OMAN {#ARABIC-OMAN}
```
public static int ARABIC_OMAN
```


Sprache: Arabisch (Oman)

### ARABIC_QATAR {#ARABIC-QATAR}
```
public static int ARABIC_QATAR
```


Sprache: Arabisch (Katar)

### ARABIC_SAUDI_ARABIA {#ARABIC-SAUDI-ARABIA}
```
public static int ARABIC_SAUDI_ARABIA
```


Sprache: Arabisch (Saudi-Arabien)

### ARABIC_SYRIA {#ARABIC-SYRIA}
```
public static int ARABIC_SYRIA
```


Sprache: Arabisch (Syrien)

### ARABIC_TUNISIA {#ARABIC-TUNISIA}
```
public static int ARABIC_TUNISIA
```


Sprache: Arabisch (Tunesien)

### ARABIC_UAE {#ARABIC-UAE}
```
public static int ARABIC_UAE
```


Sprache: Arabisch (Vereinigte Arabische Emirate)

### ARABIC_YEMEN {#ARABIC-YEMEN}
```
public static int ARABIC_YEMEN
```


Sprache: Arabisch (Jemen)

### ARMENIAN {#ARMENIAN}
```
public static int ARMENIAN
```


Sprache: Armenisch

### ASSAMESE {#ASSAMESE}
```
public static int ASSAMESE
```


Sprache: Assamesisch

### AZERBAIJANI_CYRILLIC {#AZERBAIJANI-CYRILLIC}
```
public static int AZERBAIJANI_CYRILLIC
```


Sprache: Aserbaidschanisch (Kyrillisch)

### AZERBAIJANI_LATIN {#AZERBAIJANI-LATIN}
```
public static int AZERBAIJANI_LATIN
```


Sprache: Aserbaidschanisch (Lateinisch)

### BANGLA_BANGLADESH {#BANGLA-BANGLADESH}
```
public static int BANGLA_BANGLADESH
```


Sprache: Bangla (Bangladesch)

### BANGLA_INDIA {#BANGLA-INDIA}
```
public static int BANGLA_INDIA
```


Sprache: Bangla (Indien)

### BASHKIR {#BASHKIR}
```
public static int BASHKIR
```


Sprache: Baschkirisch

### BASQUE {#BASQUE}
```
public static int BASQUE
```


Sprache: Baskisch

### BELARUSIAN {#BELARUSIAN}
```
public static int BELARUSIAN
```


Sprache: Weißrussisch

### BOSNIAN_CYRILLIC {#BOSNIAN-CYRILLIC}
```
public static int BOSNIAN_CYRILLIC
```


Sprache: Bosnisch (Kyrillisch)

### BOSNIAN_LATIN {#BOSNIAN-LATIN}
```
public static int BOSNIAN_LATIN
```


Sprache: Bosnisch (Lateinisch)

### BRETON {#BRETON}
```
public static int BRETON
```


Sprache: Bretonisch

### BULGARIAN {#BULGARIAN}
```
public static int BULGARIAN
```


Sprache: Bulgarisch

### BURMESE {#BURMESE}
```
public static int BURMESE
```


Sprache: Birmanisch

### CATALAN {#CATALAN}
```
public static int CATALAN
```


Sprache: Katalanisch

### CENTRAL_KURDISH_IRAQ {#CENTRAL-KURDISH-IRAQ}
```
public static int CENTRAL_KURDISH_IRAQ
```


Sprache: Zentral-Kurdisch (Irak)

### CHEROKEE {#CHEROKEE}
```
public static int CHEROKEE
```


Sprache: Cherokee

### CHINESE_HONG_KONG {#CHINESE-HONG-KONG}
```
public static int CHINESE_HONG_KONG
```


Sprache: Chinesisch (Hongkong)

### CHINESE_MACAO {#CHINESE-MACAO}
```
public static int CHINESE_MACAO
```


Sprache: Chinesisch (Macao)

### CHINESE_PRC {#CHINESE-PRC}
```
public static int CHINESE_PRC
```


Sprache: Chinesisch (VR China)

### CHINESE_SINGAPORE {#CHINESE-SINGAPORE}
```
public static int CHINESE_SINGAPORE
```


Sprache: Chinesisch (Singapur)

### CHINESE_TAIWAN {#CHINESE-TAIWAN}
```
public static int CHINESE_TAIWAN
```


Sprache: Chinesisch (Taiwan)

### CORSICAN {#CORSICAN}
```
public static int CORSICAN
```


Sprache: Korsisch

### CROATIAN {#CROATIAN}
```
public static int CROATIAN
```


Sprache: Kroatisch

### CROATIAN_BOZNIA_AND_HERZEGOVINA {#CROATIAN-BOZNIA-AND-HERZEGOVINA}
```
public static int CROATIAN_BOZNIA_AND_HERZEGOVINA
```


Sprache: Kroatisch (Bosnien und Herzegowina)

### CZECH {#CZECH}
```
public static int CZECH
```


Sprache: Tschechisch

### DANISH {#DANISH}
```
public static int DANISH
```


Sprache: Dänisch

### DIVEHI {#DIVEHI}
```
public static int DIVEHI
```


Sprache: Divehi

### DUTCH_BELGIUM {#DUTCH-BELGIUM}
```
public static int DUTCH_BELGIUM
```


Sprache: Niederländisch (Belgien)

### DUTCH_NETHERLANDS {#DUTCH-NETHERLANDS}
```
public static int DUTCH_NETHERLANDS
```


Sprache: Niederländisch (Niederlande)

### EDO {#EDO}
```
public static int EDO
```


Sprache: Edo

### ENGLISH_AUSTRALIA {#ENGLISH-AUSTRALIA}
```
public static int ENGLISH_AUSTRALIA
```


Sprache: Englisch (Australien)

### ENGLISH_BELIZE {#ENGLISH-BELIZE}
```
public static int ENGLISH_BELIZE
```


Sprache: Englisch (Belize)

### ENGLISH_CANADA {#ENGLISH-CANADA}
```
public static int ENGLISH_CANADA
```


Sprache: Englisch (Kanada)

### ENGLISH_CARIBBEAN {#ENGLISH-CARIBBEAN}
```
public static int ENGLISH_CARIBBEAN
```


Sprache: Englisch (Karibik)

### ENGLISH_HONG_KONG {#ENGLISH-HONG-KONG}
```
public static int ENGLISH_HONG_KONG
```


Sprache: Englisch (Hongkong)

### ENGLISH_INDIA {#ENGLISH-INDIA}
```
public static int ENGLISH_INDIA
```


Sprache: Englisch (Indien)

### ENGLISH_INDONESIA {#ENGLISH-INDONESIA}
```
public static int ENGLISH_INDONESIA
```


Sprache: Englisch (Indonesien)

### ENGLISH_IRELAND {#ENGLISH-IRELAND}
```
public static int ENGLISH_IRELAND
```


Sprache: Englisch (Irland)

### ENGLISH_JAMAICA {#ENGLISH-JAMAICA}
```
public static int ENGLISH_JAMAICA
```


Sprache: Englisch (Jamaika)

### ENGLISH_MALAYSIA {#ENGLISH-MALAYSIA}
```
public static int ENGLISH_MALAYSIA
```


Sprache: Englisch (Malaysia)

### ENGLISH_NEW_ZEALAND {#ENGLISH-NEW-ZEALAND}
```
public static int ENGLISH_NEW_ZEALAND
```


Sprache: Englisch (Neuseeland)

### ENGLISH_PHILIPPINES {#ENGLISH-PHILIPPINES}
```
public static int ENGLISH_PHILIPPINES
```


Sprache: Englisch (Philippinen)

### ENGLISH_SINGAPORE {#ENGLISH-SINGAPORE}
```
public static int ENGLISH_SINGAPORE
```


Sprache: Englisch (Singapur)

### ENGLISH_SOUTH_AFRICA {#ENGLISH-SOUTH-AFRICA}
```
public static int ENGLISH_SOUTH_AFRICA
```


Sprache: Englisch (Südafrika)

### ENGLISH_TRINIDAD_AND_TOBAGO {#ENGLISH-TRINIDAD-AND-TOBAGO}
```
public static int ENGLISH_TRINIDAD_AND_TOBAGO
```


Sprache: Englisch (Trinidad und Tobago)

### ENGLISH_UK {#ENGLISH-UK}
```
public static int ENGLISH_UK
```


Sprache: Englisch (Vereinigtes Königreich)

### ENGLISH_US {#ENGLISH-US}
```
public static int ENGLISH_US
```


Sprache: Englisch (USA)

### ENGLISH_ZIMBABWE {#ENGLISH-ZIMBABWE}
```
public static int ENGLISH_ZIMBABWE
```


Sprache: Englisch (Simbabwe)

### ESTONIAN {#ESTONIAN}
```
public static int ESTONIAN
```


Sprache: Estnisch

### FAEROESE {#FAEROESE}
```
public static int FAEROESE
```


Sprache: Färöisch

### FILIPINO {#FILIPINO}
```
public static int FILIPINO
```


Sprache: Filipino

### FINNISH {#FINNISH}
```
public static int FINNISH
```


Sprache: Finnisch

### FRENCH_BELGIUM {#FRENCH-BELGIUM}
```
public static int FRENCH_BELGIUM
```


Sprache: Französisch (Belgien)

### FRENCH_CANADA {#FRENCH-CANADA}
```
public static int FRENCH_CANADA
```


Sprache: Französisch (Kanada)

### FRENCH_FRANCE {#FRENCH-FRANCE}
```
public static int FRENCH_FRANCE
```


Sprache: Französisch (Frankreich)

### FRENCH_LUXEMBOURG {#FRENCH-LUXEMBOURG}
```
public static int FRENCH_LUXEMBOURG
```


Sprache: Französisch (Luxemburg)

### FRENCH_MONACO {#FRENCH-MONACO}
```
public static int FRENCH_MONACO
```


Sprache: Französisch (Monaco)

### FRENCH_SWITZERLAND {#FRENCH-SWITZERLAND}
```
public static int FRENCH_SWITZERLAND
```


Sprache: Französisch (Schweiz)

### FRISIAN {#FRISIAN}
```
public static int FRISIAN
```


Sprache: Friesisch

### FULAH_LATIN_SENEGAL {#FULAH-LATIN-SENEGAL}
```
public static int FULAH_LATIN_SENEGAL
```


Sprache: Fulah (Latein, Senegal)

### FULAH_NIGERIA {#FULAH-NIGERIA}
```
public static int FULAH_NIGERIA
```


Sprache: Fulah (Nigeria)

### GALICIAN {#GALICIAN}
```
public static int GALICIAN
```


Sprache: Galicisch

### GEORGIAN {#GEORGIAN}
```
public static int GEORGIAN
```


Sprache: Georgisch

### GERMAN_AUSTRIA {#GERMAN-AUSTRIA}
```
public static int GERMAN_AUSTRIA
```


Sprache: Deutsch (Österreich)

### GERMAN_GERMANY {#GERMAN-GERMANY}
```
public static int GERMAN_GERMANY
```


Sprache: Deutsch (Deutschland)

### GERMAN_LIECHTENSTEIN {#GERMAN-LIECHTENSTEIN}
```
public static int GERMAN_LIECHTENSTEIN
```


Sprache: Deutsch (Liechtenstein)

### GERMAN_LUXEMBOURG {#GERMAN-LUXEMBOURG}
```
public static int GERMAN_LUXEMBOURG
```


Sprache: Deutsch (Luxemburg)

### GERMAN_SWITZERLAND {#GERMAN-SWITZERLAND}
```
public static int GERMAN_SWITZERLAND
```


Sprache: Deutsch (Schweiz)

### GREEK {#GREEK}
```
public static int GREEK
```


Sprache: Griechisch

### GREENLANDIC {#GREENLANDIC}
```
public static int GREENLANDIC
```


Sprache: Grönländisch

### GUARANI {#GUARANI}
```
public static int GUARANI
```


Sprache: Guaraní

### GUJARATI {#GUJARATI}
```
public static int GUJARATI
```


Sprache: Gujarati

### HAUSA {#HAUSA}
```
public static int HAUSA
```


Sprache: Hausa

### HAWAIIAN {#HAWAIIAN}
```
public static int HAWAIIAN
```


Sprache: Hawaiisch

### HEBREW {#HEBREW}
```
public static int HEBREW
```


Sprache: Hebräisch

### HINDI {#HINDI}
```
public static int HINDI
```


Sprache: Hindi

### HUNGARIAN {#HUNGARIAN}
```
public static int HUNGARIAN
```


Sprache: Ungarisch

### ICELANDIC {#ICELANDIC}
```
public static int ICELANDIC
```


Sprache: Isländisch

### IGBO {#IGBO}
```
public static int IGBO
```


Sprache: Igbo

### INARI_SAMI_FINLAND {#INARI-SAMI-FINLAND}
```
public static int INARI_SAMI_FINLAND
```


Sprache: Inari-Samisch (Finnland)

### INDONESIAN {#INDONESIAN}
```
public static int INDONESIAN
```


Sprache: Indonesisch

### INUKTITUT_LATIN {#INUKTITUT-LATIN}
```
public static int INUKTITUT_LATIN
```


Sprache: Inuktitut (Latein)

### INUKTITUT_SYLLABICS {#INUKTITUT-SYLLABICS}
```
public static int INUKTITUT_SYLLABICS
```


Sprache: Inuktitut (Silben)

### IRISH {#IRISH}
```
public static int IRISH
```


Sprache: Irisch

### ISI_XHOSA {#ISI-XHOSA}
```
public static int ISI_XHOSA
```


Sprache: IsiXhosa

### ISI_ZULU {#ISI-ZULU}
```
public static int ISI_ZULU
```


Sprache: IsiZulu

### ITALIAN_ITALY {#ITALIAN-ITALY}
```
public static int ITALIAN_ITALY
```


Sprache: Italienisch (Italien)

### ITALIAN_SWITZERLAND {#ITALIAN-SWITZERLAND}
```
public static int ITALIAN_SWITZERLAND
```


Sprache: Italienisch (Schweiz)

### JAPANESE {#JAPANESE}
```
public static int JAPANESE
```


Sprache: Japanisch

### KANNADA {#KANNADA}
```
public static int KANNADA
```


Sprache: Kannada

### KANURI {#KANURI}
```
public static int KANURI
```


Sprache: Kanuri

### KASHMIRI {#KASHMIRI}
```
public static int KASHMIRI
```


Sprache: Kaschmiri

### KASHMIRI_ARABIC {#KASHMIRI-ARABIC}
```
public static int KASHMIRI_ARABIC
```


Sprache: Kaschmiri (Arabisch)

### KAZAKH {#KAZAKH}
```
public static int KAZAKH
```


Sprache: Kasachisch

### KHMER {#KHMER}
```
public static int KHMER
```


Sprache: Khmer

### KICHE {#KICHE}
```
public static int KICHE
```


Sprache: Kiche

### KINYARWANDA {#KINYARWANDA}
```
public static int KINYARWANDA
```


Sprache: Kinyarwanda

### KISWAHILI {#KISWAHILI}
```
public static int KISWAHILI
```


Sprache: Swahili

### KONKANI {#KONKANI}
```
public static int KONKANI
```


Sprache: Konkani

### KOREAN {#KOREAN}
```
public static int KOREAN
```


Sprache: Koreanisch

### KYRGYZ {#KYRGYZ}
```
public static int KYRGYZ
```


Sprache: Kirgisisch

### LAO {#LAO}
```
public static int LAO
```


Sprache: Laotisch

### LATIN {#LATIN}
```
public static int LATIN
```


Sprache: Latein

### LATVIAN {#LATVIAN}
```
public static int LATVIAN
```


Sprache: Lettisch

### LITHUANIAN {#LITHUANIAN}
```
public static int LITHUANIAN
```


Sprache: Litauisch

### LOWER_SORBIAN {#LOWER-SORBIAN}
```
public static int LOWER_SORBIAN
```


Sprache: Niedersorbisch

### LULE_SAMI_NORWAY {#LULE-SAMI-NORWAY}
```
public static int LULE_SAMI_NORWAY
```


Sprache: Lule-Sami (Norwegen)

### LULE_SAMI_SWEDEN {#LULE-SAMI-SWEDEN}
```
public static int LULE_SAMI_SWEDEN
```


Sprache: Lule-Sami (Schweden)

### LUXEMBOUGISH {#LUXEMBOUGISH}
```
public static int LUXEMBOUGISH
```


Sprache: Luxemburgisch

### MACEDONIAN {#MACEDONIAN}
```
public static int MACEDONIAN
```


Sprache: Mazedonisch

### MALAYALAM {#MALAYALAM}
```
public static int MALAYALAM
```


Sprache: Malayalam

### MALAY_BRUNEI_DARUSSALAM {#MALAY-BRUNEI-DARUSSALAM}
```
public static int MALAY_BRUNEI_DARUSSALAM
```


Sprache: Malaiisch (Brunei Darussalam)

### MALAY_MALAYSIA {#MALAY-MALAYSIA}
```
public static int MALAY_MALAYSIA
```


Sprache: Malaiisch (Malaysia)

### MALTESE {#MALTESE}
```
public static int MALTESE
```


Sprache: Maltesisch

### MANIPURI {#MANIPURI}
```
public static int MANIPURI
```


Sprache: Manipuri

### MAORI {#MAORI}
```
public static int MAORI
```


Sprache: Maori

### MAPUDUNGUN_CHILE {#MAPUDUNGUN-CHILE}
```
public static int MAPUDUNGUN_CHILE
```


Sprache: Mapudungun (Chile)

### MARATHI {#MARATHI}
```
public static int MARATHI
```


Sprache: Marathi

### MOHAWK {#MOHAWK}
```
public static int MOHAWK
```


Sprache: Mohawk

### MONGOLIAN_CYRILLIC {#MONGOLIAN-CYRILLIC}
```
public static int MONGOLIAN_CYRILLIC
```


Sprache: Mongolisch (Kyrillisch)

### MONGOLIAN_MONGOLIAN {#MONGOLIAN-MONGOLIAN}
```
public static int MONGOLIAN_MONGOLIAN
```


Sprache: Mongolisch (Mongolisch)

### NEPALI {#NEPALI}
```
public static int NEPALI
```


Sprache: Nepali

### NORTHERN_SAMI_FINLAND {#NORTHERN-SAMI-FINLAND}
```
public static int NORTHERN_SAMI_FINLAND
```


Sprache: Nordsamisch (Finnland)

### NORTHERN_SAMI_NORWAY {#NORTHERN-SAMI-NORWAY}
```
public static int NORTHERN_SAMI_NORWAY
```


Sprache: Nordsamisch (Norwegen)

### NORTHERN_SAMI_SWEDEN {#NORTHERN-SAMI-SWEDEN}
```
public static int NORTHERN_SAMI_SWEDEN
```


Sprache: Nordsamisch (Schweden)

### NORWEGIAN_BOKMAL {#NORWEGIAN-BOKMAL}
```
public static int NORWEGIAN_BOKMAL
```


Sprache: Norwegisch Bokmål

### NORWEGIAN_NYNORSK {#NORWEGIAN-NYNORSK}
```
public static int NORWEGIAN_NYNORSK
```


Sprache: Norwegisch Nynorsk

### ORIYA {#ORIYA}
```
public static int ORIYA
```


Sprache: Oriya

### OROMO {#OROMO}
```
public static int OROMO
```


Sprache: Oromo

### PAPIAMENTU {#PAPIAMENTU}
```
public static int PAPIAMENTU
```


Sprache: Papiamentu

### PASHTO {#PASHTO}
```
public static int PASHTO
```


Sprache: Paschtunisch

### PERSIAN {#PERSIAN}
```
public static int PERSIAN
```


Sprache: Persisch

### POLISH {#POLISH}
```
public static int POLISH
```


Sprache: Polnisch

### PORTUGUESE_BRAZIL {#PORTUGUESE-BRAZIL}
```
public static int PORTUGUESE_BRAZIL
```


Sprache: Portugiesisch (Brasilien)

### PORTUGUESE_PORTUGAL {#PORTUGUESE-PORTUGAL}
```
public static int PORTUGUESE_PORTUGAL
```


Sprache: Portugiesisch (Portugal)

### PUNJABI_INDIA {#PUNJABI-INDIA}
```
public static int PUNJABI_INDIA
```


Sprache: Punjabi (Indien)

### PUNJABI_PAKISTAN {#PUNJABI-PAKISTAN}
```
public static int PUNJABI_PAKISTAN
```


Sprache: Punjabi (Pakistan)

### QUECHUA_BOLIVIA {#QUECHUA-BOLIVIA}
```
public static int QUECHUA_BOLIVIA
```


Sprache: Quechua (Bolivien)

### QUECHUA_ECUADOR {#QUECHUA-ECUADOR}
```
public static int QUECHUA_ECUADOR
```


Sprache: Quechua (Ecuador)

### QUECHUA_PERU {#QUECHUA-PERU}
```
public static int QUECHUA_PERU
```


Sprache: Quechua (Peru)

### ROMANIAN {#ROMANIAN}
```
public static int ROMANIAN
```


Sprache: Rumänisch

### ROMANSH {#ROMANSH}
```
public static int ROMANSH
```


Sprache: Rätoromanisch

### RUSSIAN {#RUSSIAN}
```
public static int RUSSIAN
```


Sprache: Russisch

### SAKHA {#SAKHA}
```
public static int SAKHA
```


Sprache: Sakha

### SANSKRIT {#SANSKRIT}
```
public static int SANSKRIT
```


Sprache: Sanskrit

### SCOTTISH_GAELIC {#SCOTTISH-GAELIC}
```
public static int SCOTTISH_GAELIC
```


Sprache: Schottisch‑Gälisch

### SERBIAN_CYRILLIC_BOSNIA_AND_HERZEGOVINA {#SERBIAN-CYRILLIC-BOSNIA-AND-HERZEGOVINA}
```
public static int SERBIAN_CYRILLIC_BOSNIA_AND_HERZEGOVINA
```


Sprache: Serbisch (Kyrillisch, Bosnien und Herzegowina)

### SERBIAN_CYRILLIC_SERBIA_AND_MONTENEGRO {#SERBIAN-CYRILLIC-SERBIA-AND-MONTENEGRO}
```
public static int SERBIAN_CYRILLIC_SERBIA_AND_MONTENEGRO
```


Sprache: Serbisch (Kyrillisch, Serbien und Montenegro)

### SERBIAN_LATIN_BOSNIA_AND_HERZEGOVINA {#SERBIAN-LATIN-BOSNIA-AND-HERZEGOVINA}
```
public static int SERBIAN_LATIN_BOSNIA_AND_HERZEGOVINA
```


Sprache: Serbisch (Lateinisch, Bosnien und Herzegowina)

### SERBIAN_LATIN_SERBIA_AND_MONTENEGRO {#SERBIAN-LATIN-SERBIA-AND-MONTENEGRO}
```
public static int SERBIAN_LATIN_SERBIA_AND_MONTENEGRO
```


Sprache: Serbisch (Lateinisch, Serbien und Montenegro)

### SINDHI {#SINDHI}
```
public static int SINDHI
```


Sprache: Sindhi

### SINDHI_DEVANAGARIC {#SINDHI-DEVANAGARIC}
```
public static int SINDHI_DEVANAGARIC
```


Sprache: Sindhi (Devanagari)

### SINHALESE {#SINHALESE}
```
public static int SINHALESE
```


Sprache: Singhalesisch

### SLOVAK {#SLOVAK}
```
public static int SLOVAK
```


Sprache: Slowakisch

### SLOVENIAN {#SLOVENIAN}
```
public static int SLOVENIAN
```


Sprache: Slowenisch

### SOMALI {#SOMALI}
```
public static int SOMALI
```


Sprache: Somali

### SORBIAN {#SORBIAN}
```
public static int SORBIAN
```


Sprache: Sorbisch

### SPANISH_ARGENTINA {#SPANISH-ARGENTINA}
```
public static int SPANISH_ARGENTINA
```


Sprache: Spanisch (Argentinien)

### SPANISH_BOLIVIA {#SPANISH-BOLIVIA}
```
public static int SPANISH_BOLIVIA
```


Sprache: Spanisch (Bolivien)

### SPANISH_CHILE {#SPANISH-CHILE}
```
public static int SPANISH_CHILE
```


Sprache: Spanisch (Chile)

### SPANISH_COLOMBIA {#SPANISH-COLOMBIA}
```
public static int SPANISH_COLOMBIA
```


Sprache: Spanisch (Kolumbien)

### SPANISH_COSTA_RICA {#SPANISH-COSTA-RICA}
```
public static int SPANISH_COSTA_RICA
```


Sprache: Spanisch (Costa Rica)

### SPANISH_DOMINICAN_REPUBLIC {#SPANISH-DOMINICAN-REPUBLIC}
```
public static int SPANISH_DOMINICAN_REPUBLIC
```


Sprache: Spanisch (Dominikanische Republik)

### SPANISH_ECUADOR {#SPANISH-ECUADOR}
```
public static int SPANISH_ECUADOR
```


Sprache: Spanisch (Ecuador)

### SPANISH_EL_SALVADOR {#SPANISH-EL-SALVADOR}
```
public static int SPANISH_EL_SALVADOR
```


Sprache: Spanisch (El Salvador)

### SPANISH_GUATEMALA {#SPANISH-GUATEMALA}
```
public static int SPANISH_GUATEMALA
```


Sprache: Spanisch (Guatemala)

### SPANISH_HONDURAS {#SPANISH-HONDURAS}
```
public static int SPANISH_HONDURAS
```


Sprache: Spanisch (Honduras)

### SPANISH_MEXICO {#SPANISH-MEXICO}
```
public static int SPANISH_MEXICO
```


Sprache: Spanisch (Mexiko)

### SPANISH_NICARAGUA {#SPANISH-NICARAGUA}
```
public static int SPANISH_NICARAGUA
```


Sprache: Spanisch (Nicaragua)

### SPANISH_PANAMA {#SPANISH-PANAMA}
```
public static int SPANISH_PANAMA
```


Sprache: Spanisch (Panama)

### SPANISH_PARAGUAY {#SPANISH-PARAGUAY}
```
public static int SPANISH_PARAGUAY
```


Sprache: Spanisch (Paraguay)

### SPANISH_PERU {#SPANISH-PERU}
```
public static int SPANISH_PERU
```


Sprache: Spanisch (Peru)

### SPANISH_PUERTO_RICO {#SPANISH-PUERTO-RICO}
```
public static int SPANISH_PUERTO_RICO
```


Sprache: Spanisch (Puerto Rico)

### SPANISH_SPAIN_MODERN_SORT {#SPANISH-SPAIN-MODERN-SORT}
```
public static int SPANISH_SPAIN_MODERN_SORT
```


Sprache: Spanisch (Spanien, Moderne Sortierung)

### SPANISH_SPAIN_TRADITIONAL_SORT {#SPANISH-SPAIN-TRADITIONAL-SORT}
```
public static int SPANISH_SPAIN_TRADITIONAL_SORT
```


Sprache: Spanisch (Spanien, Traditionelle Sortierung)

### SPANISH_URUGUAY {#SPANISH-URUGUAY}
```
public static int SPANISH_URUGUAY
```


Sprache: Spanisch (Uruguay)

### SPANISH_VENEZUELA {#SPANISH-VENEZUELA}
```
public static int SPANISH_VENEZUELA
```


Sprache: Spanisch (Venezuela)

### SUTU {#SUTU}
```
public static int SUTU
```


Sprache: Sutu

### SWEDISH_FINLAND {#SWEDISH-FINLAND}
```
public static int SWEDISH_FINLAND
```


Sprache: Schwedisch (Finnland)

### SWEDISH_SWEDEN {#SWEDISH-SWEDEN}
```
public static int SWEDISH_SWEDEN
```


Sprache: Schwedisch (Schweden)

### SYRIAC {#SYRIAC}
```
public static int SYRIAC
```


Sprache: Syrisch

### TAJIK {#TAJIK}
```
public static int TAJIK
```


Sprache: Tadschikisch

### TAMAZIGHT {#TAMAZIGHT}
```
public static int TAMAZIGHT
```


Sprache: Tamazight

### TAMAZIGHT_LATIN {#TAMAZIGHT-LATIN}
```
public static int TAMAZIGHT_LATIN
```


Sprache: Tamazight (Latein)

### TAMIL {#TAMIL}
```
public static int TAMIL
```


Sprache: Tamil

### TATAR {#TATAR}
```
public static int TATAR
```


Sprache: Tatarisch

### TELUGU {#TELUGU}
```
public static int TELUGU
```


Sprache: Telugu

### THAI {#THAI}
```
public static int THAI
```


Sprache: Thai

### TIBETAN_BUTAN {#TIBETAN-BUTAN}
```
public static int TIBETAN_BUTAN
```


Sprache: Tibetisch (Bhutan)

### TIBETAN_CHINA {#TIBETAN-CHINA}
```
public static int TIBETAN_CHINA
```


Sprache: Tibetisch (China)

### TIGRIGNA_ERITREA {#TIGRIGNA-ERITREA}
```
public static int TIGRIGNA_ERITREA
```


Sprache: Tigrinya (Eritrea)

### TIGRIGNA_ETHIOPIA {#TIGRIGNA-ETHIOPIA}
```
public static int TIGRIGNA_ETHIOPIA
```


Sprache: Tigrinya (Äthiopien)

### TSONGA {#TSONGA}
```
public static int TSONGA
```


Sprache: Tsonga

### TSWANA {#TSWANA}
```
public static int TSWANA
```


Sprache: Tswana

### TURKISH {#TURKISH}
```
public static int TURKISH
```


Sprache: Türkisch

### TURKMEN {#TURKMEN}
```
public static int TURKMEN
```


Sprache: Turkmenisch

### UKRAINIAN {#UKRAINIAN}
```
public static int UKRAINIAN
```


Sprache: Ukrainisch

### URDU {#URDU}
```
public static int URDU
```


Sprache: Urdu

### UZBEK_CYRILLIC {#UZBEK-CYRILLIC}
```
public static int UZBEK_CYRILLIC
```


Sprache: Usbekisch (Kyrillisch)

### UZBEK_LATIN {#UZBEK-LATIN}
```
public static int UZBEK_LATIN
```


Sprache: Usbekisch (Lateinisch)

### VENDA {#VENDA}
```
public static int VENDA
```


Sprache: Venda

### VIETNAMESE {#VIETNAMESE}
```
public static int VIETNAMESE
```


Sprache: Vietnamesisch

### WELSH {#WELSH}
```
public static int WELSH
```


Sprache: Walisisch

### YI {#YI}
```
public static int YI
```


Sprache: Yi

### YIDDISH {#YIDDISH}
```
public static int YIDDISH
```


Sprache: Jiddisch

### YORUBA {#YORUBA}
```
public static int YORUBA
```


Sprache: Yoruba

### length {#length}
```
public static int length
```


### fromName(String editingLanguageName) {#fromName-java.lang.String}
```
public static int fromName(String editingLanguageName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| editingLanguageName | java.lang.String |  |

**Returns:**
int
### getName(int editingLanguage) {#getName-int}
```
public static String getName(int editingLanguage)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| editingLanguage | int |  |

**Returns:**
java.lang.String
