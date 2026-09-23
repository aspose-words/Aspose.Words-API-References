---
title: "EditingLanguage"
linktitle: "EditingLanguage"
second_title: "Aspose.Words per Java"
description: "Specifica la lingua di modifica in Java."
type: docs
weight: 182
url: /it/java/com.aspose.words/editinglanguage/
---

**Inheritance:**
java.lang.Object
```
public class EditingLanguage
```

Specifica la lingua di modifica.

 **Examples:** 

Mostra come applicare le preferenze di lingua durante il caricamento di un documento.

```

 LoadOptions loadOptions = new LoadOptions();
 loadOptions.getLanguagePreferences().addEditingLanguage(EditingLanguage.JAPANESE);

 Document doc = new Document(getMyDir() + "No default editing language.docx", loadOptions);

 int localeIdFarEast = doc.getStyles().getDefaultFont().getLocaleIdFarEast();
 System.out.println(localeIdFarEast == EditingLanguage.JAPANESE
         ? "The document either has no any FarEast language set in defaults or it was set to Japanese originally."
         : "The document default FarEast language was set to another than Japanese language originally, so it is not overridden.");
 
```
## Campi

| Campo | Descrizione |
| --- | --- |
| [AFRIKAANS](#AFRIKAANS) | Lingua: Afrikaans |
| [ALBANIAN](#ALBANIAN) | Lingua: Albanese |
| [ALSATIAN](#ALSATIAN) | Lingua: Alsaziano |
| [AMHARIC](#AMHARIC) | Lingua: Amarico |
| [ARABIC_ALGERIA](#ARABIC-ALGERIA) | Lingua: Arabo (Algeria) |
| [ARABIC_BAHRAIN](#ARABIC-BAHRAIN) | Lingua: Arabo (Bahrein) |
| [ARABIC_EGYPT](#ARABIC-EGYPT) | Lingua: Arabo (Egitto) |
| [ARABIC_IRAQ](#ARABIC-IRAQ) | Lingua: Arabo (Iraq) |
| [ARABIC_JORDAN](#ARABIC-JORDAN) | Lingua: arabo (Giordania) |
| [ARABIC_KUWAIT](#ARABIC-KUWAIT) | Lingua: arabo (Kuwait) |
| [ARABIC_LEBANON](#ARABIC-LEBANON) | Lingua: arabo (Libano) |
| [ARABIC_LIBYA](#ARABIC-LIBYA) | Lingua: arabo (Libia) |
| [ARABIC_MOROCCO](#ARABIC-MOROCCO) | Lingua: arabo (Marocco) |
| [ARABIC_OMAN](#ARABIC-OMAN) | Lingua: arabo (Oman) |
| [ARABIC_QATAR](#ARABIC-QATAR) | Lingua: arabo (Qatar) |
| [ARABIC_SAUDI_ARABIA](#ARABIC-SAUDI-ARABIA) | Lingua: arabo (Arabia Saudita) |
| [ARABIC_SYRIA](#ARABIC-SYRIA) | Lingua: arabo (Siria) |
| [ARABIC_TUNISIA](#ARABIC-TUNISIA) | Lingua: arabo (Tunisia) |
| [ARABIC_UAE](#ARABIC-UAE) | Lingua: arabo (Emirati Arabi Uniti) |
| [ARABIC_YEMEN](#ARABIC-YEMEN) | Lingua: arabo (Yemen) |
| [ARMENIAN](#ARMENIAN) | Lingua: armeno |
| [ASSAMESE](#ASSAMESE) | Lingua: assamese |
| [AZERBAIJANI_CYRILLIC](#AZERBAIJANI-CYRILLIC) | Lingua: azero (cirillico) |
| [AZERBAIJANI_LATIN](#AZERBAIJANI-LATIN) | Lingua: azero (latino) |
| [BANGLA_BANGLADESH](#BANGLA-BANGLADESH) | Lingua: bengalese (Bangladesh) |
| [BANGLA_INDIA](#BANGLA-INDIA) | Lingua: bengalese (India) |
| [BASHKIR](#BASHKIR) | Lingua: baschiro |
| [BASQUE](#BASQUE) | Lingua: basco |
| [BELARUSIAN](#BELARUSIAN) | Lingua: bielorusso |
| [BOSNIAN_CYRILLIC](#BOSNIAN-CYRILLIC) | Lingua: bosniaco (cirillico) |
| [BOSNIAN_LATIN](#BOSNIAN-LATIN) | Lingua: bosniaco (latino) |
| [BRETON](#BRETON) | Lingua: bretone |
| [BULGARIAN](#BULGARIAN) | Lingua: bulgaro |
| [BURMESE](#BURMESE) | Lingua: Birmano |
| [CATALAN](#CATALAN) | Lingua: Catalano |
| [CENTRAL_KURDISH_IRAQ](#CENTRAL-KURDISH-IRAQ) | Lingua: Curdo centrale (Iraq) |
| [CHEROKEE](#CHEROKEE) | Lingua: Cherokee |
| [CHINESE_HONG_KONG](#CHINESE-HONG-KONG) | Lingua: Cinese (Hong Kong) |
| [CHINESE_MACAO](#CHINESE-MACAO) | Lingua: Cinese (Macao) |
| [CHINESE_PRC](#CHINESE-PRC) | Lingua: Cinese (RPC) |
| [CHINESE_SINGAPORE](#CHINESE-SINGAPORE) | Lingua: Cinese (Singapore) |
| [CHINESE_TAIWAN](#CHINESE-TAIWAN) | Lingua: Cinese (Taiwan) |
| [CORSICAN](#CORSICAN) | Lingua: Corso |
| [CROATIAN](#CROATIAN) | Lingua: Croato |
| [CROATIAN_BOZNIA_AND_HERZEGOVINA](#CROATIAN-BOZNIA-AND-HERZEGOVINA) | Lingua: Croato (Bosnia ed Erzegovina) |
| [CZECH](#CZECH) | Lingua: Ceco |
| [DANISH](#DANISH) | Lingua: Danese |
| [DIVEHI](#DIVEHI) | Lingua: Divehi |
| [DUTCH_BELGIUM](#DUTCH-BELGIUM) | Lingua: Olandese (Belgio) |
| [DUTCH_NETHERLANDS](#DUTCH-NETHERLANDS) | Lingua: Olandese (Paesi Bassi) |
| [EDO](#EDO) | Lingua: Edo |
| [ENGLISH_AUSTRALIA](#ENGLISH-AUSTRALIA) | Lingua: Inglese (Australia) |
| [ENGLISH_BELIZE](#ENGLISH-BELIZE) | Lingua: Inglese (Belize) |
| [ENGLISH_CANADA](#ENGLISH-CANADA) | Lingua: Inglese (Canada) |
| [ENGLISH_CARIBBEAN](#ENGLISH-CARIBBEAN) | Lingua: Inglese (Caraibi) |
| [ENGLISH_HONG_KONG](#ENGLISH-HONG-KONG) | Lingua: Inglese (Hong Kong) |
| [ENGLISH_INDIA](#ENGLISH-INDIA) | Lingua: Inglese (India) |
| [ENGLISH_INDONESIA](#ENGLISH-INDONESIA) | Lingua: Inglese (Indonesia) |
| [ENGLISH_IRELAND](#ENGLISH-IRELAND) | Lingua: Inglese (Irlanda) |
| [ENGLISH_JAMAICA](#ENGLISH-JAMAICA) | Lingua: Inglese (Giamaica) |
| [ENGLISH_MALAYSIA](#ENGLISH-MALAYSIA) | Lingua: Inglese (Malesia) |
| [ENGLISH_NEW_ZEALAND](#ENGLISH-NEW-ZEALAND) | Lingua: Inglese (Nuova Zelanda) |
| [ENGLISH_PHILIPPINES](#ENGLISH-PHILIPPINES) | Lingua: Inglese (Filippine) |
| [ENGLISH_SINGAPORE](#ENGLISH-SINGAPORE) | Lingua: Inglese (Singapore) |
| [ENGLISH_SOUTH_AFRICA](#ENGLISH-SOUTH-AFRICA) | Lingua: Inglese (Sudafrica) |
| [ENGLISH_TRINIDAD_AND_TOBAGO](#ENGLISH-TRINIDAD-AND-TOBAGO) | Lingua: Inglese (Trinidad e Tobago) |
| [ENGLISH_UK](#ENGLISH-UK) | Lingua: Inglese (Regno Unito) |
| [ENGLISH_US](#ENGLISH-US) | Lingua: Inglese (Stati Uniti) |
| [ENGLISH_ZIMBABWE](#ENGLISH-ZIMBABWE) | Lingua: Inglese (Zimbabwe) |
| [ESTONIAN](#ESTONIAN) | Lingua: Estone |
| [FAEROESE](#FAEROESE) | Lingua: Faroese |
| [FILIPINO](#FILIPINO) | Lingua: Filippino |
| [FINNISH](#FINNISH) | Lingua: Finlandese |
| [FRENCH_BELGIUM](#FRENCH-BELGIUM) | Lingua: Francese (Belgio) |
| [FRENCH_CANADA](#FRENCH-CANADA) | Lingua: Francese (Canada) |
| [FRENCH_FRANCE](#FRENCH-FRANCE) | Lingua: Francese (Francia) |
| [FRENCH_LUXEMBOURG](#FRENCH-LUXEMBOURG) | Lingua: Francese (Lussemburgo) |
| [FRENCH_MONACO](#FRENCH-MONACO) | Lingua: Francese (Monaco) |
| [FRENCH_SWITZERLAND](#FRENCH-SWITZERLAND) | Lingua: Francese (Svizzera) |
| [FRISIAN](#FRISIAN) | Lingua: Frisone |
| [FULAH_LATIN_SENEGAL](#FULAH-LATIN-SENEGAL) | Lingua: Fulah (Latino, Senegal) |
| [FULAH_NIGERIA](#FULAH-NIGERIA) | Lingua: Fulah (Nigeria) |
| [GALICIAN](#GALICIAN) | Lingua: Galiziano |
| [GEORGIAN](#GEORGIAN) | Lingua: georgiano |
| [GERMAN_AUSTRIA](#GERMAN-AUSTRIA) | Lingua: tedesco (Austria) |
| [GERMAN_GERMANY](#GERMAN-GERMANY) | Lingua: tedesco (Germania) |
| [GERMAN_LIECHTENSTEIN](#GERMAN-LIECHTENSTEIN) | Lingua: tedesco (Liechtenstein) |
| [GERMAN_LUXEMBOURG](#GERMAN-LUXEMBOURG) | Lingua: tedesco (Lussemburgo) |
| [GERMAN_SWITZERLAND](#GERMAN-SWITZERLAND) | Lingua: tedesco (Svizzera) |
| [GREEK](#GREEK) | Lingua: greco |
| [GREENLANDIC](#GREENLANDIC) | Lingua: groenlandese |
| [GUARANI](#GUARANI) | Lingua: guaraní |
| [GUJARATI](#GUJARATI) | Lingua: gujarati |
| [HAUSA](#HAUSA) | Lingua: hausa |
| [HAWAIIAN](#HAWAIIAN) | Lingua: hawaiano |
| [HEBREW](#HEBREW) | Lingua: ebraico |
| [HINDI](#HINDI) | Lingua: hindi |
| [HUNGARIAN](#HUNGARIAN) | Lingua: ungherese |
| [ICELANDIC](#ICELANDIC) | Lingua: islandese |
| [IGBO](#IGBO) | Lingua: igbo |
| [INARI_SAMI_FINLAND](#INARI-SAMI-FINLAND) | Lingua: Sami Inari (Finlandia) |
| [INDONESIAN](#INDONESIAN) | Lingua: indonesiano |
| [INUKTITUT_LATIN](#INUKTITUT-LATIN) | Lingua: Inuktitut (Latino) |
| [INUKTITUT_SYLLABICS](#INUKTITUT-SYLLABICS) | Lingua: Inuktitut (Sillabico) |
| [IRISH](#IRISH) | Lingua: irlandese |
| [ISI_XHOSA](#ISI-XHOSA) | Lingua: isiXhosa |
| [ISI_ZULU](#ISI-ZULU) | Lingua: isiZulu |
| [ITALIAN_ITALY](#ITALIAN-ITALY) | Lingua: Italiano (Italia) |
| [ITALIAN_SWITZERLAND](#ITALIAN-SWITZERLAND) | Lingua: Italiano (Svizzera) |
| [JAPANESE](#JAPANESE) | Lingua: Giapponese |
| [KANNADA](#KANNADA) | Lingua: Kannada |
| [KANURI](#KANURI) | Lingua: Kanuri |
| [KASHMIRI](#KASHMIRI) | Lingua: Kashmiri |
| [KASHMIRI_ARABIC](#KASHMIRI-ARABIC) | Lingua: Kashmiri (Arabo) |
| [KAZAKH](#KAZAKH) | Lingua: Kazako |
| [KHMER](#KHMER) | Lingua: Khmer |
| [KICHE](#KICHE) | Lingua: Kiche |
| [KINYARWANDA](#KINYARWANDA) | Lingua: Kinyarwanda |
| [KISWAHILI](#KISWAHILI) | Lingua: Kiswahili |
| [KONKANI](#KONKANI) | Lingua: Konkani |
| [KOREAN](#KOREAN) | Lingua: Coreano |
| [KYRGYZ](#KYRGYZ) | Lingua: Kirghiso |
| [LAO](#LAO) | Lingua: Lao |
| [LATIN](#LATIN) | Lingua: Latino |
| [LATVIAN](#LATVIAN) | Lingua: Lettone |
| [LITHUANIAN](#LITHUANIAN) | Lingua: Lituano |
| [LOWER_SORBIAN](#LOWER-SORBIAN) | Lingua: Sorabo inferiore |
| [LULE_SAMI_NORWAY](#LULE-SAMI-NORWAY) | Lingua: Sami di Lule (Norvegia) |
| [LULE_SAMI_SWEDEN](#LULE-SAMI-SWEDEN) | Lingua: Sami di Lule (Svezia) |
| [LUXEMBOUGISH](#LUXEMBOUGISH) | Lingua: Lussemburghese |
| [MACEDONIAN](#MACEDONIAN) | Lingua: Macedone |
| [MALAYALAM](#MALAYALAM) | Lingua: Malayalam |
| [MALAY_BRUNEI_DARUSSALAM](#MALAY-BRUNEI-DARUSSALAM) | Lingua: Malese (Brunei Darussalam) |
| [MALAY_MALAYSIA](#MALAY-MALAYSIA) | Lingua: Malese (Malesia) |
| [MALTESE](#MALTESE) | Lingua: Maltese |
| [MANIPURI](#MANIPURI) | Lingua: Manipuri |
| [MAORI](#MAORI) | Lingua: Maori |
| [MAPUDUNGUN_CHILE](#MAPUDUNGUN-CHILE) | Lingua: Mapudungun (Cile) |
| [MARATHI](#MARATHI) | Lingua: Marathi |
| [MOHAWK](#MOHAWK) | Lingua: Mohawk |
| [MONGOLIAN_CYRILLIC](#MONGOLIAN-CYRILLIC) | Lingua: Mongolo (Cirillico) |
| [MONGOLIAN_MONGOLIAN](#MONGOLIAN-MONGOLIAN) | Lingua: Mongolo (Mongolo) |
| [NEPALI](#NEPALI) | Lingua: Nepalese |
| [NORTHERN_SAMI_FINLAND](#NORTHERN-SAMI-FINLAND) | Lingua: Sami settentrionale (Finlandia) |
| [NORTHERN_SAMI_NORWAY](#NORTHERN-SAMI-NORWAY) | Lingua: Sami settentrionale (Norvegia) |
| [NORTHERN_SAMI_SWEDEN](#NORTHERN-SAMI-SWEDEN) | Lingua: Sami settentrionale (Svezia) |
| [NORWEGIAN_BOKMAL](#NORWEGIAN-BOKMAL) | Lingua: Norvegese Bokmål |
| [NORWEGIAN_NYNORSK](#NORWEGIAN-NYNORSK) | Lingua: Norvegese Nynorsk |
| [ORIYA](#ORIYA) | Lingua: Oriya |
| [OROMO](#OROMO) | Lingua: Oromo |
| [PAPIAMENTU](#PAPIAMENTU) | Lingua: Papiamento |
| [PASHTO](#PASHTO) | Lingua: Pashto |
| [PERSIAN](#PERSIAN) | Lingua: Persiano |
| [POLISH](#POLISH) | Lingua: Polacco |
| [PORTUGUESE_BRAZIL](#PORTUGUESE-BRAZIL) | Lingua: Portoghese (Brasile) |
| [PORTUGUESE_PORTUGAL](#PORTUGUESE-PORTUGAL) | Lingua: Portoghese (Portogallo) |
| [PUNJABI_INDIA](#PUNJABI-INDIA) | Lingua: Punjabi (India) |
| [PUNJABI_PAKISTAN](#PUNJABI-PAKISTAN) | Lingua: Punjabi (Pakistan) |
| [QUECHUA_BOLIVIA](#QUECHUA-BOLIVIA) | Lingua: Quechua (Bolivia) |
| [QUECHUA_ECUADOR](#QUECHUA-ECUADOR) | Lingua: Quechua (Ecuador) |
| [QUECHUA_PERU](#QUECHUA-PERU) | Lingua: Quechua (Perù) |
| [ROMANIAN](#ROMANIAN) | Lingua: Rumeno |
| [ROMANSH](#ROMANSH) | Lingua: Rumantsch |
| [RUSSIAN](#RUSSIAN) | Lingua: Russo |
| [SAKHA](#SAKHA) | Lingua: Sakha |
| [SANSKRIT](#SANSKRIT) | Lingua: Sanscrito |
| [SCOTTISH_GAELIC](#SCOTTISH-GAELIC) | Lingua: Gaelico scozzese |
| [SERBIAN_CYRILLIC_BOSNIA_AND_HERZEGOVINA](#SERBIAN-CYRILLIC-BOSNIA-AND-HERZEGOVINA) | Lingua: Serbo (Cirillico, Bosnia ed Erzegovina) |
| [SERBIAN_CYRILLIC_SERBIA_AND_MONTENEGRO](#SERBIAN-CYRILLIC-SERBIA-AND-MONTENEGRO) | Lingua: Serbo (Cirillico, Serbia e Montenegro) |
| [SERBIAN_LATIN_BOSNIA_AND_HERZEGOVINA](#SERBIAN-LATIN-BOSNIA-AND-HERZEGOVINA) | Lingua: Serbo (Latino, Bosnia ed Erzegovina) |
| [SERBIAN_LATIN_SERBIA_AND_MONTENEGRO](#SERBIAN-LATIN-SERBIA-AND-MONTENEGRO) | Lingua: Serbo (Latino, Serbia e Montenegro) |
| [SINDHI](#SINDHI) | Lingua: Sindhi |
| [SINDHI_DEVANAGARIC](#SINDHI-DEVANAGARIC) | Lingua: Sindhi (Devanagari) |
| [SINHALESE](#SINHALESE) | Lingua: Singalese |
| [SLOVAK](#SLOVAK) | Lingua: Slovacco |
| [SLOVENIAN](#SLOVENIAN) | Lingua: Sloveno |
| [SOMALI](#SOMALI) | Lingua: Somalo |
| [SORBIAN](#SORBIAN) | Lingua: Sorabo |
| [SPANISH_ARGENTINA](#SPANISH-ARGENTINA) | Lingua: Spagnolo (Argentina) |
| [SPANISH_BOLIVIA](#SPANISH-BOLIVIA) | Lingua: Spagnolo (Bolivia) |
| [SPANISH_CHILE](#SPANISH-CHILE) | Lingua: Spagnolo (Cile) |
| [SPANISH_COLOMBIA](#SPANISH-COLOMBIA) | Lingua: Spagnolo (Colombia) |
| [SPANISH_COSTA_RICA](#SPANISH-COSTA-RICA) | Lingua: Spagnolo (Costa Rica) |
| [SPANISH_DOMINICAN_REPUBLIC](#SPANISH-DOMINICAN-REPUBLIC) | Lingua: spagnolo (Repubblica Dominicana) |
| [SPANISH_ECUADOR](#SPANISH-ECUADOR) | Lingua: spagnolo (Ecuador) |
| [SPANISH_EL_SALVADOR](#SPANISH-EL-SALVADOR) | Lingua: spagnolo (El Salvador) |
| [SPANISH_GUATEMALA](#SPANISH-GUATEMALA) | Lingua: spagnolo (Guatemala) |
| [SPANISH_HONDURAS](#SPANISH-HONDURAS) | Lingua: spagnolo (Honduras) |
| [SPANISH_MEXICO](#SPANISH-MEXICO) | Lingua: spagnolo (Messico) |
| [SPANISH_NICARAGUA](#SPANISH-NICARAGUA) | Lingua: spagnolo (Nicaragua) |
| [SPANISH_PANAMA](#SPANISH-PANAMA) | Lingua: spagnolo (Panama) |
| [SPANISH_PARAGUAY](#SPANISH-PARAGUAY) | Lingua: spagnolo (Paraguay) |
| [SPANISH_PERU](#SPANISH-PERU) | Lingua: spagnolo (Perù) |
| [SPANISH_PUERTO_RICO](#SPANISH-PUERTO-RICO) | Lingua: spagnolo (Porto Rico) |
| [SPANISH_SPAIN_MODERN_SORT](#SPANISH-SPAIN-MODERN-SORT) | Lingua: spagnolo (Spagna, ordinamento moderno) |
| [SPANISH_SPAIN_TRADITIONAL_SORT](#SPANISH-SPAIN-TRADITIONAL-SORT) | Lingua: spagnolo (Spagna, ordinamento tradizionale) |
| [SPANISH_URUGUAY](#SPANISH-URUGUAY) | Lingua: spagnolo (Uruguay) |
| [SPANISH_VENEZUELA](#SPANISH-VENEZUELA) | Lingua: spagnolo (Venezuela) |
| [SUTU](#SUTU) | Lingua: Sutu |
| [SWEDISH_FINLAND](#SWEDISH-FINLAND) | Lingua: svedese (Finlandia) |
| [SWEDISH_SWEDEN](#SWEDISH-SWEDEN) | Lingua: svedese (Svezia) |
| [SYRIAC](#SYRIAC) | Lingua: siriaco |
| [TAJIK](#TAJIK) | Lingua: tagico |
| [TAMAZIGHT](#TAMAZIGHT) | Lingua: tamazight |
| [TAMAZIGHT_LATIN](#TAMAZIGHT-LATIN) | Lingua: tamazight (latino) |
| [TAMIL](#TAMIL) | Lingua: tamil |
| [TATAR](#TATAR) | Lingua: tartaro |
| [TELUGU](#TELUGU) | Lingua: telugu |
| [THAI](#THAI) | Lingua: Thai |
| [TIBETAN_BUTAN](#TIBETAN-BUTAN) | Lingua: Tibetan (Bhutan) |
| [TIBETAN_CHINA](#TIBETAN-CHINA) | Lingua: Tibetan (China) |
| [TIGRIGNA_ERITREA](#TIGRIGNA-ERITREA) | Lingua: Tigrigna (Eritrea) |
| [TIGRIGNA_ETHIOPIA](#TIGRIGNA-ETHIOPIA) | Lingua: Tigrigna (Ethiopia) |
| [TSONGA](#TSONGA) | Lingua: Tsonga |
| [TSWANA](#TSWANA) | Lingua: Tswana |
| [TURKISH](#TURKISH) | Lingua: Turkish |
| [TURKMEN](#TURKMEN) | Lingua: Turkmen |
| [UKRAINIAN](#UKRAINIAN) | Lingua: Ukrainian |
| [URDU](#URDU) | Lingua: Urdu |
| [UZBEK_CYRILLIC](#UZBEK-CYRILLIC) | Lingua: Uzbek (Cyrillic) |
| [UZBEK_LATIN](#UZBEK-LATIN) | Lingua: Uzbek (Latin) |
| [VENDA](#VENDA) | Lingua: Venda |
| [VIETNAMESE](#VIETNAMESE) | Lingua: Vietnamese |
| [WELSH](#WELSH) | Lingua: Welsh |
| [YI](#YI) | Lingua: Yi |
| [YIDDISH](#YIDDISH) | Lingua: Yiddish |
| [YORUBA](#YORUBA) | Lingua: Yoruba |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String editingLanguageName)](#fromName-java.lang.String) |  |
| [getName(int editingLanguage)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int editingLanguage)](#toString-int) |  |
### AFRIKAANS {#AFRIKAANS}
```
public static int AFRIKAANS
```


Lingua: Afrikaans

### ALBANIAN {#ALBANIAN}
```
public static int ALBANIAN
```


Lingua: Albanese

### ALSATIAN {#ALSATIAN}
```
public static int ALSATIAN
```


Lingua: Alsaziano

### AMHARIC {#AMHARIC}
```
public static int AMHARIC
```


Lingua: Amarico

### ARABIC_ALGERIA {#ARABIC-ALGERIA}
```
public static int ARABIC_ALGERIA
```


Lingua: Arabo (Algeria)

### ARABIC_BAHRAIN {#ARABIC-BAHRAIN}
```
public static int ARABIC_BAHRAIN
```


Lingua: Arabo (Bahrein)

### ARABIC_EGYPT {#ARABIC-EGYPT}
```
public static int ARABIC_EGYPT
```


Lingua: Arabo (Egitto)

### ARABIC_IRAQ {#ARABIC-IRAQ}
```
public static int ARABIC_IRAQ
```


Lingua: Arabo (Iraq)

### ARABIC_JORDAN {#ARABIC-JORDAN}
```
public static int ARABIC_JORDAN
```


Lingua: arabo (Giordania)

### ARABIC_KUWAIT {#ARABIC-KUWAIT}
```
public static int ARABIC_KUWAIT
```


Lingua: arabo (Kuwait)

### ARABIC_LEBANON {#ARABIC-LEBANON}
```
public static int ARABIC_LEBANON
```


Lingua: arabo (Libano)

### ARABIC_LIBYA {#ARABIC-LIBYA}
```
public static int ARABIC_LIBYA
```


Lingua: arabo (Libia)

### ARABIC_MOROCCO {#ARABIC-MOROCCO}
```
public static int ARABIC_MOROCCO
```


Lingua: arabo (Marocco)

### ARABIC_OMAN {#ARABIC-OMAN}
```
public static int ARABIC_OMAN
```


Lingua: arabo (Oman)

### ARABIC_QATAR {#ARABIC-QATAR}
```
public static int ARABIC_QATAR
```


Lingua: arabo (Qatar)

### ARABIC_SAUDI_ARABIA {#ARABIC-SAUDI-ARABIA}
```
public static int ARABIC_SAUDI_ARABIA
```


Lingua: arabo (Arabia Saudita)

### ARABIC_SYRIA {#ARABIC-SYRIA}
```
public static int ARABIC_SYRIA
```


Lingua: arabo (Siria)

### ARABIC_TUNISIA {#ARABIC-TUNISIA}
```
public static int ARABIC_TUNISIA
```


Lingua: arabo (Tunisia)

### ARABIC_UAE {#ARABIC-UAE}
```
public static int ARABIC_UAE
```


Lingua: arabo (Emirati Arabi Uniti)

### ARABIC_YEMEN {#ARABIC-YEMEN}
```
public static int ARABIC_YEMEN
```


Lingua: arabo (Yemen)

### ARMENIAN {#ARMENIAN}
```
public static int ARMENIAN
```


Lingua: armeno

### ASSAMESE {#ASSAMESE}
```
public static int ASSAMESE
```


Lingua: assamese

### AZERBAIJANI_CYRILLIC {#AZERBAIJANI-CYRILLIC}
```
public static int AZERBAIJANI_CYRILLIC
```


Lingua: azero (cirillico)

### AZERBAIJANI_LATIN {#AZERBAIJANI-LATIN}
```
public static int AZERBAIJANI_LATIN
```


Lingua: azero (latino)

### BANGLA_BANGLADESH {#BANGLA-BANGLADESH}
```
public static int BANGLA_BANGLADESH
```


Lingua: bengalese (Bangladesh)

### BANGLA_INDIA {#BANGLA-INDIA}
```
public static int BANGLA_INDIA
```


Lingua: bengalese (India)

### BASHKIR {#BASHKIR}
```
public static int BASHKIR
```


Lingua: baschiro

### BASQUE {#BASQUE}
```
public static int BASQUE
```


Lingua: basco

### BELARUSIAN {#BELARUSIAN}
```
public static int BELARUSIAN
```


Lingua: bielorusso

### BOSNIAN_CYRILLIC {#BOSNIAN-CYRILLIC}
```
public static int BOSNIAN_CYRILLIC
```


Lingua: bosniaco (cirillico)

### BOSNIAN_LATIN {#BOSNIAN-LATIN}
```
public static int BOSNIAN_LATIN
```


Lingua: bosniaco (latino)

### BRETON {#BRETON}
```
public static int BRETON
```


Lingua: bretone

### BULGARIAN {#BULGARIAN}
```
public static int BULGARIAN
```


Lingua: bulgaro

### BURMESE {#BURMESE}
```
public static int BURMESE
```


Lingua: Birmano

### CATALAN {#CATALAN}
```
public static int CATALAN
```


Lingua: Catalano

### CENTRAL_KURDISH_IRAQ {#CENTRAL-KURDISH-IRAQ}
```
public static int CENTRAL_KURDISH_IRAQ
```


Lingua: Curdo centrale (Iraq)

### CHEROKEE {#CHEROKEE}
```
public static int CHEROKEE
```


Lingua: Cherokee

### CHINESE_HONG_KONG {#CHINESE-HONG-KONG}
```
public static int CHINESE_HONG_KONG
```


Lingua: Cinese (Hong Kong)

### CHINESE_MACAO {#CHINESE-MACAO}
```
public static int CHINESE_MACAO
```


Lingua: Cinese (Macao)

### CHINESE_PRC {#CHINESE-PRC}
```
public static int CHINESE_PRC
```


Lingua: Cinese (RPC)

### CHINESE_SINGAPORE {#CHINESE-SINGAPORE}
```
public static int CHINESE_SINGAPORE
```


Lingua: Cinese (Singapore)

### CHINESE_TAIWAN {#CHINESE-TAIWAN}
```
public static int CHINESE_TAIWAN
```


Lingua: Cinese (Taiwan)

### CORSICAN {#CORSICAN}
```
public static int CORSICAN
```


Lingua: Corso

### CROATIAN {#CROATIAN}
```
public static int CROATIAN
```


Lingua: Croato

### CROATIAN_BOZNIA_AND_HERZEGOVINA {#CROATIAN-BOZNIA-AND-HERZEGOVINA}
```
public static int CROATIAN_BOZNIA_AND_HERZEGOVINA
```


Lingua: Croato (Bosnia ed Erzegovina)

### CZECH {#CZECH}
```
public static int CZECH
```


Lingua: Ceco

### DANISH {#DANISH}
```
public static int DANISH
```


Lingua: Danese

### DIVEHI {#DIVEHI}
```
public static int DIVEHI
```


Lingua: Divehi

### DUTCH_BELGIUM {#DUTCH-BELGIUM}
```
public static int DUTCH_BELGIUM
```


Lingua: Olandese (Belgio)

### DUTCH_NETHERLANDS {#DUTCH-NETHERLANDS}
```
public static int DUTCH_NETHERLANDS
```


Lingua: Olandese (Paesi Bassi)

### EDO {#EDO}
```
public static int EDO
```


Lingua: Edo

### ENGLISH_AUSTRALIA {#ENGLISH-AUSTRALIA}
```
public static int ENGLISH_AUSTRALIA
```


Lingua: Inglese (Australia)

### ENGLISH_BELIZE {#ENGLISH-BELIZE}
```
public static int ENGLISH_BELIZE
```


Lingua: Inglese (Belize)

### ENGLISH_CANADA {#ENGLISH-CANADA}
```
public static int ENGLISH_CANADA
```


Lingua: Inglese (Canada)

### ENGLISH_CARIBBEAN {#ENGLISH-CARIBBEAN}
```
public static int ENGLISH_CARIBBEAN
```


Lingua: Inglese (Caraibi)

### ENGLISH_HONG_KONG {#ENGLISH-HONG-KONG}
```
public static int ENGLISH_HONG_KONG
```


Lingua: Inglese (Hong Kong)

### ENGLISH_INDIA {#ENGLISH-INDIA}
```
public static int ENGLISH_INDIA
```


Lingua: Inglese (India)

### ENGLISH_INDONESIA {#ENGLISH-INDONESIA}
```
public static int ENGLISH_INDONESIA
```


Lingua: Inglese (Indonesia)

### ENGLISH_IRELAND {#ENGLISH-IRELAND}
```
public static int ENGLISH_IRELAND
```


Lingua: Inglese (Irlanda)

### ENGLISH_JAMAICA {#ENGLISH-JAMAICA}
```
public static int ENGLISH_JAMAICA
```


Lingua: Inglese (Giamaica)

### ENGLISH_MALAYSIA {#ENGLISH-MALAYSIA}
```
public static int ENGLISH_MALAYSIA
```


Lingua: Inglese (Malesia)

### ENGLISH_NEW_ZEALAND {#ENGLISH-NEW-ZEALAND}
```
public static int ENGLISH_NEW_ZEALAND
```


Lingua: Inglese (Nuova Zelanda)

### ENGLISH_PHILIPPINES {#ENGLISH-PHILIPPINES}
```
public static int ENGLISH_PHILIPPINES
```


Lingua: Inglese (Filippine)

### ENGLISH_SINGAPORE {#ENGLISH-SINGAPORE}
```
public static int ENGLISH_SINGAPORE
```


Lingua: Inglese (Singapore)

### ENGLISH_SOUTH_AFRICA {#ENGLISH-SOUTH-AFRICA}
```
public static int ENGLISH_SOUTH_AFRICA
```


Lingua: Inglese (Sudafrica)

### ENGLISH_TRINIDAD_AND_TOBAGO {#ENGLISH-TRINIDAD-AND-TOBAGO}
```
public static int ENGLISH_TRINIDAD_AND_TOBAGO
```


Lingua: Inglese (Trinidad e Tobago)

### ENGLISH_UK {#ENGLISH-UK}
```
public static int ENGLISH_UK
```


Lingua: Inglese (Regno Unito)

### ENGLISH_US {#ENGLISH-US}
```
public static int ENGLISH_US
```


Lingua: Inglese (Stati Uniti)

### ENGLISH_ZIMBABWE {#ENGLISH-ZIMBABWE}
```
public static int ENGLISH_ZIMBABWE
```


Lingua: Inglese (Zimbabwe)

### ESTONIAN {#ESTONIAN}
```
public static int ESTONIAN
```


Lingua: Estone

### FAEROESE {#FAEROESE}
```
public static int FAEROESE
```


Lingua: Faroese

### FILIPINO {#FILIPINO}
```
public static int FILIPINO
```


Lingua: Filippino

### FINNISH {#FINNISH}
```
public static int FINNISH
```


Lingua: Finlandese

### FRENCH_BELGIUM {#FRENCH-BELGIUM}
```
public static int FRENCH_BELGIUM
```


Lingua: Francese (Belgio)

### FRENCH_CANADA {#FRENCH-CANADA}
```
public static int FRENCH_CANADA
```


Lingua: Francese (Canada)

### FRENCH_FRANCE {#FRENCH-FRANCE}
```
public static int FRENCH_FRANCE
```


Lingua: Francese (Francia)

### FRENCH_LUXEMBOURG {#FRENCH-LUXEMBOURG}
```
public static int FRENCH_LUXEMBOURG
```


Lingua: Francese (Lussemburgo)

### FRENCH_MONACO {#FRENCH-MONACO}
```
public static int FRENCH_MONACO
```


Lingua: Francese (Monaco)

### FRENCH_SWITZERLAND {#FRENCH-SWITZERLAND}
```
public static int FRENCH_SWITZERLAND
```


Lingua: Francese (Svizzera)

### FRISIAN {#FRISIAN}
```
public static int FRISIAN
```


Lingua: Frisone

### FULAH_LATIN_SENEGAL {#FULAH-LATIN-SENEGAL}
```
public static int FULAH_LATIN_SENEGAL
```


Lingua: Fulah (Latino, Senegal)

### FULAH_NIGERIA {#FULAH-NIGERIA}
```
public static int FULAH_NIGERIA
```


Lingua: Fulah (Nigeria)

### GALICIAN {#GALICIAN}
```
public static int GALICIAN
```


Lingua: Galiziano

### GEORGIAN {#GEORGIAN}
```
public static int GEORGIAN
```


Lingua: georgiano

### GERMAN_AUSTRIA {#GERMAN-AUSTRIA}
```
public static int GERMAN_AUSTRIA
```


Lingua: tedesco (Austria)

### GERMAN_GERMANY {#GERMAN-GERMANY}
```
public static int GERMAN_GERMANY
```


Lingua: tedesco (Germania)

### GERMAN_LIECHTENSTEIN {#GERMAN-LIECHTENSTEIN}
```
public static int GERMAN_LIECHTENSTEIN
```


Lingua: tedesco (Liechtenstein)

### GERMAN_LUXEMBOURG {#GERMAN-LUXEMBOURG}
```
public static int GERMAN_LUXEMBOURG
```


Lingua: tedesco (Lussemburgo)

### GERMAN_SWITZERLAND {#GERMAN-SWITZERLAND}
```
public static int GERMAN_SWITZERLAND
```


Lingua: tedesco (Svizzera)

### GREEK {#GREEK}
```
public static int GREEK
```


Lingua: greco

### GREENLANDIC {#GREENLANDIC}
```
public static int GREENLANDIC
```


Lingua: groenlandese

### GUARANI {#GUARANI}
```
public static int GUARANI
```


Lingua: guaraní

### GUJARATI {#GUJARATI}
```
public static int GUJARATI
```


Lingua: gujarati

### HAUSA {#HAUSA}
```
public static int HAUSA
```


Lingua: hausa

### HAWAIIAN {#HAWAIIAN}
```
public static int HAWAIIAN
```


Lingua: hawaiano

### HEBREW {#HEBREW}
```
public static int HEBREW
```


Lingua: ebraico

### HINDI {#HINDI}
```
public static int HINDI
```


Lingua: hindi

### HUNGARIAN {#HUNGARIAN}
```
public static int HUNGARIAN
```


Lingua: ungherese

### ICELANDIC {#ICELANDIC}
```
public static int ICELANDIC
```


Lingua: islandese

### IGBO {#IGBO}
```
public static int IGBO
```


Lingua: igbo

### INARI_SAMI_FINLAND {#INARI-SAMI-FINLAND}
```
public static int INARI_SAMI_FINLAND
```


Lingua: Sami Inari (Finlandia)

### INDONESIAN {#INDONESIAN}
```
public static int INDONESIAN
```


Lingua: indonesiano

### INUKTITUT_LATIN {#INUKTITUT-LATIN}
```
public static int INUKTITUT_LATIN
```


Lingua: Inuktitut (Latino)

### INUKTITUT_SYLLABICS {#INUKTITUT-SYLLABICS}
```
public static int INUKTITUT_SYLLABICS
```


Lingua: Inuktitut (Sillabico)

### IRISH {#IRISH}
```
public static int IRISH
```


Lingua: irlandese

### ISI_XHOSA {#ISI-XHOSA}
```
public static int ISI_XHOSA
```


Lingua: isiXhosa

### ISI_ZULU {#ISI-ZULU}
```
public static int ISI_ZULU
```


Lingua: isiZulu

### ITALIAN_ITALY {#ITALIAN-ITALY}
```
public static int ITALIAN_ITALY
```


Lingua: Italiano (Italia)

### ITALIAN_SWITZERLAND {#ITALIAN-SWITZERLAND}
```
public static int ITALIAN_SWITZERLAND
```


Lingua: Italiano (Svizzera)

### JAPANESE {#JAPANESE}
```
public static int JAPANESE
```


Lingua: Giapponese

### KANNADA {#KANNADA}
```
public static int KANNADA
```


Lingua: Kannada

### KANURI {#KANURI}
```
public static int KANURI
```


Lingua: Kanuri

### KASHMIRI {#KASHMIRI}
```
public static int KASHMIRI
```


Lingua: Kashmiri

### KASHMIRI_ARABIC {#KASHMIRI-ARABIC}
```
public static int KASHMIRI_ARABIC
```


Lingua: Kashmiri (Arabo)

### KAZAKH {#KAZAKH}
```
public static int KAZAKH
```


Lingua: Kazako

### KHMER {#KHMER}
```
public static int KHMER
```


Lingua: Khmer

### KICHE {#KICHE}
```
public static int KICHE
```


Lingua: Kiche

### KINYARWANDA {#KINYARWANDA}
```
public static int KINYARWANDA
```


Lingua: Kinyarwanda

### KISWAHILI {#KISWAHILI}
```
public static int KISWAHILI
```


Lingua: Kiswahili

### KONKANI {#KONKANI}
```
public static int KONKANI
```


Lingua: Konkani

### KOREAN {#KOREAN}
```
public static int KOREAN
```


Lingua: Coreano

### KYRGYZ {#KYRGYZ}
```
public static int KYRGYZ
```


Lingua: Kirghiso

### LAO {#LAO}
```
public static int LAO
```


Lingua: Lao

### LATIN {#LATIN}
```
public static int LATIN
```


Lingua: Latino

### LATVIAN {#LATVIAN}
```
public static int LATVIAN
```


Lingua: Lettone

### LITHUANIAN {#LITHUANIAN}
```
public static int LITHUANIAN
```


Lingua: Lituano

### LOWER_SORBIAN {#LOWER-SORBIAN}
```
public static int LOWER_SORBIAN
```


Lingua: Sorabo inferiore

### LULE_SAMI_NORWAY {#LULE-SAMI-NORWAY}
```
public static int LULE_SAMI_NORWAY
```


Lingua: Sami di Lule (Norvegia)

### LULE_SAMI_SWEDEN {#LULE-SAMI-SWEDEN}
```
public static int LULE_SAMI_SWEDEN
```


Lingua: Sami di Lule (Svezia)

### LUXEMBOUGISH {#LUXEMBOUGISH}
```
public static int LUXEMBOUGISH
```


Lingua: Lussemburghese

### MACEDONIAN {#MACEDONIAN}
```
public static int MACEDONIAN
```


Lingua: Macedone

### MALAYALAM {#MALAYALAM}
```
public static int MALAYALAM
```


Lingua: Malayalam

### MALAY_BRUNEI_DARUSSALAM {#MALAY-BRUNEI-DARUSSALAM}
```
public static int MALAY_BRUNEI_DARUSSALAM
```


Lingua: Malese (Brunei Darussalam)

### MALAY_MALAYSIA {#MALAY-MALAYSIA}
```
public static int MALAY_MALAYSIA
```


Lingua: Malese (Malesia)

### MALTESE {#MALTESE}
```
public static int MALTESE
```


Lingua: Maltese

### MANIPURI {#MANIPURI}
```
public static int MANIPURI
```


Lingua: Manipuri

### MAORI {#MAORI}
```
public static int MAORI
```


Lingua: Maori

### MAPUDUNGUN_CHILE {#MAPUDUNGUN-CHILE}
```
public static int MAPUDUNGUN_CHILE
```


Lingua: Mapudungun (Cile)

### MARATHI {#MARATHI}
```
public static int MARATHI
```


Lingua: Marathi

### MOHAWK {#MOHAWK}
```
public static int MOHAWK
```


Lingua: Mohawk

### MONGOLIAN_CYRILLIC {#MONGOLIAN-CYRILLIC}
```
public static int MONGOLIAN_CYRILLIC
```


Lingua: Mongolo (Cirillico)

### MONGOLIAN_MONGOLIAN {#MONGOLIAN-MONGOLIAN}
```
public static int MONGOLIAN_MONGOLIAN
```


Lingua: Mongolo (Mongolo)

### NEPALI {#NEPALI}
```
public static int NEPALI
```


Lingua: Nepalese

### NORTHERN_SAMI_FINLAND {#NORTHERN-SAMI-FINLAND}
```
public static int NORTHERN_SAMI_FINLAND
```


Lingua: Sami settentrionale (Finlandia)

### NORTHERN_SAMI_NORWAY {#NORTHERN-SAMI-NORWAY}
```
public static int NORTHERN_SAMI_NORWAY
```


Lingua: Sami settentrionale (Norvegia)

### NORTHERN_SAMI_SWEDEN {#NORTHERN-SAMI-SWEDEN}
```
public static int NORTHERN_SAMI_SWEDEN
```


Lingua: Sami settentrionale (Svezia)

### NORWEGIAN_BOKMAL {#NORWEGIAN-BOKMAL}
```
public static int NORWEGIAN_BOKMAL
```


Lingua: Norvegese Bokmål

### NORWEGIAN_NYNORSK {#NORWEGIAN-NYNORSK}
```
public static int NORWEGIAN_NYNORSK
```


Lingua: Norvegese Nynorsk

### ORIYA {#ORIYA}
```
public static int ORIYA
```


Lingua: Oriya

### OROMO {#OROMO}
```
public static int OROMO
```


Lingua: Oromo

### PAPIAMENTU {#PAPIAMENTU}
```
public static int PAPIAMENTU
```


Lingua: Papiamento

### PASHTO {#PASHTO}
```
public static int PASHTO
```


Lingua: Pashto

### PERSIAN {#PERSIAN}
```
public static int PERSIAN
```


Lingua: Persiano

### POLISH {#POLISH}
```
public static int POLISH
```


Lingua: Polacco

### PORTUGUESE_BRAZIL {#PORTUGUESE-BRAZIL}
```
public static int PORTUGUESE_BRAZIL
```


Lingua: Portoghese (Brasile)

### PORTUGUESE_PORTUGAL {#PORTUGUESE-PORTUGAL}
```
public static int PORTUGUESE_PORTUGAL
```


Lingua: Portoghese (Portogallo)

### PUNJABI_INDIA {#PUNJABI-INDIA}
```
public static int PUNJABI_INDIA
```


Lingua: Punjabi (India)

### PUNJABI_PAKISTAN {#PUNJABI-PAKISTAN}
```
public static int PUNJABI_PAKISTAN
```


Lingua: Punjabi (Pakistan)

### QUECHUA_BOLIVIA {#QUECHUA-BOLIVIA}
```
public static int QUECHUA_BOLIVIA
```


Lingua: Quechua (Bolivia)

### QUECHUA_ECUADOR {#QUECHUA-ECUADOR}
```
public static int QUECHUA_ECUADOR
```


Lingua: Quechua (Ecuador)

### QUECHUA_PERU {#QUECHUA-PERU}
```
public static int QUECHUA_PERU
```


Lingua: Quechua (Perù)

### ROMANIAN {#ROMANIAN}
```
public static int ROMANIAN
```


Lingua: Rumeno

### ROMANSH {#ROMANSH}
```
public static int ROMANSH
```


Lingua: Rumantsch

### RUSSIAN {#RUSSIAN}
```
public static int RUSSIAN
```


Lingua: Russo

### SAKHA {#SAKHA}
```
public static int SAKHA
```


Lingua: Sakha

### SANSKRIT {#SANSKRIT}
```
public static int SANSKRIT
```


Lingua: Sanscrito

### SCOTTISH_GAELIC {#SCOTTISH-GAELIC}
```
public static int SCOTTISH_GAELIC
```


Lingua: Gaelico scozzese

### SERBIAN_CYRILLIC_BOSNIA_AND_HERZEGOVINA {#SERBIAN-CYRILLIC-BOSNIA-AND-HERZEGOVINA}
```
public static int SERBIAN_CYRILLIC_BOSNIA_AND_HERZEGOVINA
```


Lingua: Serbo (Cirillico, Bosnia ed Erzegovina)

### SERBIAN_CYRILLIC_SERBIA_AND_MONTENEGRO {#SERBIAN-CYRILLIC-SERBIA-AND-MONTENEGRO}
```
public static int SERBIAN_CYRILLIC_SERBIA_AND_MONTENEGRO
```


Lingua: Serbo (Cirillico, Serbia e Montenegro)

### SERBIAN_LATIN_BOSNIA_AND_HERZEGOVINA {#SERBIAN-LATIN-BOSNIA-AND-HERZEGOVINA}
```
public static int SERBIAN_LATIN_BOSNIA_AND_HERZEGOVINA
```


Lingua: Serbo (Latino, Bosnia ed Erzegovina)

### SERBIAN_LATIN_SERBIA_AND_MONTENEGRO {#SERBIAN-LATIN-SERBIA-AND-MONTENEGRO}
```
public static int SERBIAN_LATIN_SERBIA_AND_MONTENEGRO
```


Lingua: Serbo (Latino, Serbia e Montenegro)

### SINDHI {#SINDHI}
```
public static int SINDHI
```


Lingua: Sindhi

### SINDHI_DEVANAGARIC {#SINDHI-DEVANAGARIC}
```
public static int SINDHI_DEVANAGARIC
```


Lingua: Sindhi (Devanagari)

### SINHALESE {#SINHALESE}
```
public static int SINHALESE
```


Lingua: Singalese

### SLOVAK {#SLOVAK}
```
public static int SLOVAK
```


Lingua: Slovacco

### SLOVENIAN {#SLOVENIAN}
```
public static int SLOVENIAN
```


Lingua: Sloveno

### SOMALI {#SOMALI}
```
public static int SOMALI
```


Lingua: Somalo

### SORBIAN {#SORBIAN}
```
public static int SORBIAN
```


Lingua: Sorabo

### SPANISH_ARGENTINA {#SPANISH-ARGENTINA}
```
public static int SPANISH_ARGENTINA
```


Lingua: Spagnolo (Argentina)

### SPANISH_BOLIVIA {#SPANISH-BOLIVIA}
```
public static int SPANISH_BOLIVIA
```


Lingua: Spagnolo (Bolivia)

### SPANISH_CHILE {#SPANISH-CHILE}
```
public static int SPANISH_CHILE
```


Lingua: Spagnolo (Cile)

### SPANISH_COLOMBIA {#SPANISH-COLOMBIA}
```
public static int SPANISH_COLOMBIA
```


Lingua: Spagnolo (Colombia)

### SPANISH_COSTA_RICA {#SPANISH-COSTA-RICA}
```
public static int SPANISH_COSTA_RICA
```


Lingua: Spagnolo (Costa Rica)

### SPANISH_DOMINICAN_REPUBLIC {#SPANISH-DOMINICAN-REPUBLIC}
```
public static int SPANISH_DOMINICAN_REPUBLIC
```


Lingua: spagnolo (Repubblica Dominicana)

### SPANISH_ECUADOR {#SPANISH-ECUADOR}
```
public static int SPANISH_ECUADOR
```


Lingua: spagnolo (Ecuador)

### SPANISH_EL_SALVADOR {#SPANISH-EL-SALVADOR}
```
public static int SPANISH_EL_SALVADOR
```


Lingua: spagnolo (El Salvador)

### SPANISH_GUATEMALA {#SPANISH-GUATEMALA}
```
public static int SPANISH_GUATEMALA
```


Lingua: spagnolo (Guatemala)

### SPANISH_HONDURAS {#SPANISH-HONDURAS}
```
public static int SPANISH_HONDURAS
```


Lingua: spagnolo (Honduras)

### SPANISH_MEXICO {#SPANISH-MEXICO}
```
public static int SPANISH_MEXICO
```


Lingua: spagnolo (Messico)

### SPANISH_NICARAGUA {#SPANISH-NICARAGUA}
```
public static int SPANISH_NICARAGUA
```


Lingua: spagnolo (Nicaragua)

### SPANISH_PANAMA {#SPANISH-PANAMA}
```
public static int SPANISH_PANAMA
```


Lingua: spagnolo (Panama)

### SPANISH_PARAGUAY {#SPANISH-PARAGUAY}
```
public static int SPANISH_PARAGUAY
```


Lingua: spagnolo (Paraguay)

### SPANISH_PERU {#SPANISH-PERU}
```
public static int SPANISH_PERU
```


Lingua: spagnolo (Perù)

### SPANISH_PUERTO_RICO {#SPANISH-PUERTO-RICO}
```
public static int SPANISH_PUERTO_RICO
```


Lingua: spagnolo (Porto Rico)

### SPANISH_SPAIN_MODERN_SORT {#SPANISH-SPAIN-MODERN-SORT}
```
public static int SPANISH_SPAIN_MODERN_SORT
```


Lingua: spagnolo (Spagna, ordinamento moderno)

### SPANISH_SPAIN_TRADITIONAL_SORT {#SPANISH-SPAIN-TRADITIONAL-SORT}
```
public static int SPANISH_SPAIN_TRADITIONAL_SORT
```


Lingua: spagnolo (Spagna, ordinamento tradizionale)

### SPANISH_URUGUAY {#SPANISH-URUGUAY}
```
public static int SPANISH_URUGUAY
```


Lingua: spagnolo (Uruguay)

### SPANISH_VENEZUELA {#SPANISH-VENEZUELA}
```
public static int SPANISH_VENEZUELA
```


Lingua: spagnolo (Venezuela)

### SUTU {#SUTU}
```
public static int SUTU
```


Lingua: Sutu

### SWEDISH_FINLAND {#SWEDISH-FINLAND}
```
public static int SWEDISH_FINLAND
```


Lingua: svedese (Finlandia)

### SWEDISH_SWEDEN {#SWEDISH-SWEDEN}
```
public static int SWEDISH_SWEDEN
```


Lingua: svedese (Svezia)

### SYRIAC {#SYRIAC}
```
public static int SYRIAC
```


Lingua: siriaco

### TAJIK {#TAJIK}
```
public static int TAJIK
```


Lingua: tagico

### TAMAZIGHT {#TAMAZIGHT}
```
public static int TAMAZIGHT
```


Lingua: tamazight

### TAMAZIGHT_LATIN {#TAMAZIGHT-LATIN}
```
public static int TAMAZIGHT_LATIN
```


Lingua: tamazight (latino)

### TAMIL {#TAMIL}
```
public static int TAMIL
```


Lingua: tamil

### TATAR {#TATAR}
```
public static int TATAR
```


Lingua: tartaro

### TELUGU {#TELUGU}
```
public static int TELUGU
```


Lingua: telugu

### THAI {#THAI}
```
public static int THAI
```


Lingua: Thai

### TIBETAN_BUTAN {#TIBETAN-BUTAN}
```
public static int TIBETAN_BUTAN
```


Lingua: Tibetan (Bhutan)

### TIBETAN_CHINA {#TIBETAN-CHINA}
```
public static int TIBETAN_CHINA
```


Lingua: Tibetan (China)

### TIGRIGNA_ERITREA {#TIGRIGNA-ERITREA}
```
public static int TIGRIGNA_ERITREA
```


Lingua: Tigrigna (Eritrea)

### TIGRIGNA_ETHIOPIA {#TIGRIGNA-ETHIOPIA}
```
public static int TIGRIGNA_ETHIOPIA
```


Lingua: Tigrigna (Ethiopia)

### TSONGA {#TSONGA}
```
public static int TSONGA
```


Lingua: Tsonga

### TSWANA {#TSWANA}
```
public static int TSWANA
```


Lingua: Tswana

### TURKISH {#TURKISH}
```
public static int TURKISH
```


Lingua: Turkish

### TURKMEN {#TURKMEN}
```
public static int TURKMEN
```


Lingua: Turkmen

### UKRAINIAN {#UKRAINIAN}
```
public static int UKRAINIAN
```


Lingua: Ukrainian

### URDU {#URDU}
```
public static int URDU
```


Lingua: Urdu

### UZBEK_CYRILLIC {#UZBEK-CYRILLIC}
```
public static int UZBEK_CYRILLIC
```


Lingua: Uzbek (Cyrillic)

### UZBEK_LATIN {#UZBEK-LATIN}
```
public static int UZBEK_LATIN
```


Lingua: Uzbek (Latin)

### VENDA {#VENDA}
```
public static int VENDA
```


Lingua: Venda

### VIETNAMESE {#VIETNAMESE}
```
public static int VIETNAMESE
```


Lingua: Vietnamese

### WELSH {#WELSH}
```
public static int WELSH
```


Lingua: Welsh

### YI {#YI}
```
public static int YI
```


Lingua: Yi

### YIDDISH {#YIDDISH}
```
public static int YIDDISH
```


Lingua: Yiddish

### YORUBA {#YORUBA}
```
public static int YORUBA
```


Lingua: Yoruba

### length {#length}
```
public static int length
```


### fromName(String editingLanguageName) {#fromName-java.lang.String}
```
public static int fromName(String editingLanguageName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| editingLanguageName | java.lang.String |  |

**Returns:**
int
### getName(int editingLanguage) {#getName-int}
```
public static String getName(int editingLanguage)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| editingLanguage | int |  |

**Returns:**
java.lang.String
