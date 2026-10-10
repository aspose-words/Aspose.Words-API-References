---
title: "EditingLanguage"
linktitle: "EditingLanguage"
second_title: "Aspose.Words para Java"
description: "Especifica el idioma de edición en Java."
type: docs
weight: 182
url: /es/java/com.aspose.words/editinglanguage/
---

**Inheritance:**
java.lang.Object
```
public class EditingLanguage
```

Especifica el idioma de edición.

 **Examples:** 

Muestra cómo aplicar preferencias de idioma al cargar un documento.

```

 LoadOptions loadOptions = new LoadOptions();
 loadOptions.getLanguagePreferences().addEditingLanguage(EditingLanguage.JAPANESE);

 Document doc = new Document(getMyDir() + "No default editing language.docx", loadOptions);

 int localeIdFarEast = doc.getStyles().getDefaultFont().getLocaleIdFarEast();
 System.out.println(localeIdFarEast == EditingLanguage.JAPANESE
         ? "The document either has no any FarEast language set in defaults or it was set to Japanese originally."
         : "The document default FarEast language was set to another than Japanese language originally, so it is not overridden.");
 
```
## Campos

| Campo | Descripción |
| --- | --- |
| [AFRIKAANS](#AFRIKAANS) | Idioma: Afrikaans |
| [ALBANIAN](#ALBANIAN) | Idioma: Albanés |
| [ALSATIAN](#ALSATIAN) | Idioma: Alsaciano |
| [AMHARIC](#AMHARIC) | Idioma: Amhárico |
| [ARABIC_ALGERIA](#ARABIC-ALGERIA) | Idioma: Árabe (Argelia) |
| [ARABIC_BAHRAIN](#ARABIC-BAHRAIN) | Idioma: Árabe (Baréin) |
| [ARABIC_EGYPT](#ARABIC-EGYPT) | Idioma: Árabe (Egipto) |
| [ARABIC_IRAQ](#ARABIC-IRAQ) | Idioma: Árabe (Irak) |
| [ARABIC_JORDAN](#ARABIC-JORDAN) | Idioma: Árabe (Jordania) |
| [ARABIC_KUWAIT](#ARABIC-KUWAIT) | Idioma: Árabe (Kuwait) |
| [ARABIC_LEBANON](#ARABIC-LEBANON) | Idioma: Árabe (Líbano) |
| [ARABIC_LIBYA](#ARABIC-LIBYA) | Idioma: Árabe (Libia) |
| [ARABIC_MOROCCO](#ARABIC-MOROCCO) | Idioma: Árabe (Marruecos) |
| [ARABIC_OMAN](#ARABIC-OMAN) | Idioma: Árabe (Omán) |
| [ARABIC_QATAR](#ARABIC-QATAR) | Idioma: Árabe (Catar) |
| [ARABIC_SAUDI_ARABIA](#ARABIC-SAUDI-ARABIA) | Idioma: Árabe (Arabia Saudita) |
| [ARABIC_SYRIA](#ARABIC-SYRIA) | Idioma: Árabe (Siria) |
| [ARABIC_TUNISIA](#ARABIC-TUNISIA) | Idioma: Árabe (Túnez) |
| [ARABIC_UAE](#ARABIC-UAE) | Idioma: Árabe (Emiratos Árabes Unidos) |
| [ARABIC_YEMEN](#ARABIC-YEMEN) | Idioma: Árabe (Yemen) |
| [ARMENIAN](#ARMENIAN) | Idioma: Armenio |
| [ASSAMESE](#ASSAMESE) | Idioma: Asamés |
| [AZERBAIJANI_CYRILLIC](#AZERBAIJANI-CYRILLIC) | Idioma: Azerbaiyano (Cirílico) |
| [AZERBAIJANI_LATIN](#AZERBAIJANI-LATIN) | Idioma: Azerbaiyano (Latín) |
| [BANGLA_BANGLADESH](#BANGLA-BANGLADESH) | Idioma: Bengalí (Bangladés) |
| [BANGLA_INDIA](#BANGLA-INDIA) | Idioma: Bengalí (India) |
| [BASHKIR](#BASHKIR) | Idioma: Bashkir |
| [BASQUE](#BASQUE) | Idioma: Vasco |
| [BELARUSIAN](#BELARUSIAN) | Idioma: Bielorruso |
| [BOSNIAN_CYRILLIC](#BOSNIAN-CYRILLIC) | Idioma: Bosnio (Cirílico) |
| [BOSNIAN_LATIN](#BOSNIAN-LATIN) | Idioma: Bosnio (Latín) |
| [BRETON](#BRETON) | Idioma: Bretón |
| [BULGARIAN](#BULGARIAN) | Idioma: Búlgaro |
| [BURMESE](#BURMESE) | Idioma: Birmano |
| [CATALAN](#CATALAN) | Idioma: Catalán |
| [CENTRAL_KURDISH_IRAQ](#CENTRAL-KURDISH-IRAQ) | Idioma: Kurdo central (Irak) |
| [CHEROKEE](#CHEROKEE) | Idioma: Cherokee |
| [CHINESE_HONG_KONG](#CHINESE-HONG-KONG) | Idioma: Chino (Hong Kong) |
| [CHINESE_MACAO](#CHINESE-MACAO) | Idioma: Chino (Macao) |
| [CHINESE_PRC](#CHINESE-PRC) | Idioma: Chino (RPC) |
| [CHINESE_SINGAPORE](#CHINESE-SINGAPORE) | Idioma: Chino (Singapur) |
| [CHINESE_TAIWAN](#CHINESE-TAIWAN) | Idioma: Chino (Taiwán) |
| [CORSICAN](#CORSICAN) | Idioma: Corso |
| [CROATIAN](#CROATIAN) | Idioma: Croata |
| [CROATIAN_BOZNIA_AND_HERZEGOVINA](#CROATIAN-BOZNIA-AND-HERZEGOVINA) | Idioma: Croata (Bosnia y Herzegovina) |
| [CZECH](#CZECH) | Idioma: Checo |
| [DANISH](#DANISH) | Idioma: Danés |
| [DIVEHI](#DIVEHI) | Idioma: Divehi |
| [DUTCH_BELGIUM](#DUTCH-BELGIUM) | Idioma: Holandés (Bélgica) |
| [DUTCH_NETHERLANDS](#DUTCH-NETHERLANDS) | Idioma: Holandés (Países Bajos) |
| [EDO](#EDO) | Idioma: Edo |
| [ENGLISH_AUSTRALIA](#ENGLISH-AUSTRALIA) | Idioma: Inglés (Australia) |
| [ENGLISH_BELIZE](#ENGLISH-BELIZE) | Idioma: Inglés (Belice) |
| [ENGLISH_CANADA](#ENGLISH-CANADA) | Idioma: Inglés (Canadá) |
| [ENGLISH_CARIBBEAN](#ENGLISH-CARIBBEAN) | Idioma: Inglés (Caribe) |
| [ENGLISH_HONG_KONG](#ENGLISH-HONG-KONG) | Idioma: Inglés (Hong Kong) |
| [ENGLISH_INDIA](#ENGLISH-INDIA) | Idioma: Inglés (India) |
| [ENGLISH_INDONESIA](#ENGLISH-INDONESIA) | Idioma: Inglés (Indonesia) |
| [ENGLISH_IRELAND](#ENGLISH-IRELAND) | Idioma: Inglés (Irlanda) |
| [ENGLISH_JAMAICA](#ENGLISH-JAMAICA) | Idioma: Inglés (Jamaica) |
| [ENGLISH_MALAYSIA](#ENGLISH-MALAYSIA) | Idioma: Inglés (Malasia) |
| [ENGLISH_NEW_ZEALAND](#ENGLISH-NEW-ZEALAND) | Idioma: Inglés (Nueva Zelanda) |
| [ENGLISH_PHILIPPINES](#ENGLISH-PHILIPPINES) | Idioma: Inglés (Filipinas) |
| [ENGLISH_SINGAPORE](#ENGLISH-SINGAPORE) | Idioma: Inglés (Singapur) |
| [ENGLISH_SOUTH_AFRICA](#ENGLISH-SOUTH-AFRICA) | Idioma: Inglés (Sudáfrica) |
| [ENGLISH_TRINIDAD_AND_TOBAGO](#ENGLISH-TRINIDAD-AND-TOBAGO) | Idioma: Inglés (Trinidad y Tobago) |
| [ENGLISH_UK](#ENGLISH-UK) | Idioma: Inglés (Reino Unido) |
| [ENGLISH_US](#ENGLISH-US) | Idioma: Inglés (EE. UU.) |
| [ENGLISH_ZIMBABWE](#ENGLISH-ZIMBABWE) | Idioma: Inglés (Zimbabue) |
| [ESTONIAN](#ESTONIAN) | Estonio |
| [FAEROESE](#FAEROESE) | Feroés |
| [FILIPINO](#FILIPINO) | Filipino |
| [FINNISH](#FINNISH) | Finlandés |
| [FRENCH_BELGIUM](#FRENCH-BELGIUM) | Francés (Bélgica) |
| [FRENCH_CANADA](#FRENCH-CANADA) | Francés (Canadá) |
| [FRENCH_FRANCE](#FRENCH-FRANCE) | Francés (Francia) |
| [FRENCH_LUXEMBOURG](#FRENCH-LUXEMBOURG) | Francés (Luxemburgo) |
| [FRENCH_MONACO](#FRENCH-MONACO) | Francés (Mónaco) |
| [FRENCH_SWITZERLAND](#FRENCH-SWITZERLAND) | Francés (Suiza) |
| [FRISIAN](#FRISIAN) | Frisón |
| [FULAH_LATIN_SENEGAL](#FULAH-LATIN-SENEGAL) | Fulah (Latín, Senegal) |
| [FULAH_NIGERIA](#FULAH-NIGERIA) | Fulah (Nigeria) |
| [GALICIAN](#GALICIAN) | Gallego |
| [GEORGIAN](#GEORGIAN) | Idioma: georgiano |
| [GERMAN_AUSTRIA](#GERMAN-AUSTRIA) | Idioma: alemán (Austria) |
| [GERMAN_GERMANY](#GERMAN-GERMANY) | Idioma: alemán (Alemania) |
| [GERMAN_LIECHTENSTEIN](#GERMAN-LIECHTENSTEIN) | Idioma: alemán (Liechtenstein) |
| [GERMAN_LUXEMBOURG](#GERMAN-LUXEMBOURG) | Idioma: alemán (Luxemburgo) |
| [GERMAN_SWITZERLAND](#GERMAN-SWITZERLAND) | Idioma: alemán (Suiza) |
| [GREEK](#GREEK) | Idioma: griego |
| [GREENLANDIC](#GREENLANDIC) | Idioma: groenlandés |
| [GUARANI](#GUARANI) | Idioma: guaraní |
| [GUJARATI](#GUJARATI) | Idioma: gujarati |
| [HAUSA](#HAUSA) | Idioma: hausa |
| [HAWAIIAN](#HAWAIIAN) | Idioma: hawaiano |
| [HEBREW](#HEBREW) | Idioma: hebreo |
| [HINDI](#HINDI) | Idioma: hindi |
| [HUNGARIAN](#HUNGARIAN) | Idioma: húngaro |
| [ICELANDIC](#ICELANDIC) | Idioma: islandés |
| [IGBO](#IGBO) | Idioma: igbo |
| [INARI_SAMI_FINLAND](#INARI-SAMI-FINLAND) | Idioma: Inari Sami (Finlandia) |
| [INDONESIAN](#INDONESIAN) | Idioma: indonesio |
| [INUKTITUT_LATIN](#INUKTITUT-LATIN) | Idioma: inuktitut (Latín) |
| [INUKTITUT_SYLLABICS](#INUKTITUT-SYLLABICS) | Idioma: inuktitut (Silábico) |
| [IRISH](#IRISH) | Idioma: irlandés |
| [ISI_XHOSA](#ISI-XHOSA) | Idioma: isiXhosa |
| [ISI_ZULU](#ISI-ZULU) | Idioma: isiZulu |
| [ITALIAN_ITALY](#ITALIAN-ITALY) | Idioma: italiano (Italia) |
| [ITALIAN_SWITZERLAND](#ITALIAN-SWITZERLAND) | Idioma: italiano (Suiza) |
| [JAPANESE](#JAPANESE) | Idioma: japonés |
| [KANNADA](#KANNADA) | Idioma: kannada |
| [KANURI](#KANURI) | Idioma: kanuri |
| [KASHMIRI](#KASHMIRI) | Idioma: cachemiro |
| [KASHMIRI_ARABIC](#KASHMIRI-ARABIC) | Idioma: cachemiro (árabe) |
| [KAZAKH](#KAZAKH) | Idioma: kazajo |
| [KHMER](#KHMER) | Idioma: jemer |
| [KICHE](#KICHE) | Idioma: k'iche' |
| [KINYARWANDA](#KINYARWANDA) | Idioma: kinyarwanda |
| [KISWAHILI](#KISWAHILI) | Idioma: kiswahili |
| [KONKANI](#KONKANI) | Idioma: konkani |
| [KOREAN](#KOREAN) | Idioma: coreano |
| [KYRGYZ](#KYRGYZ) | Idioma: kirguís |
| [LAO](#LAO) | Idioma: lao |
| [LATIN](#LATIN) | Idioma: latín |
| [LATVIAN](#LATVIAN) | Idioma: letón |
| [LITHUANIAN](#LITHUANIAN) | Idioma: lituano |
| [LOWER_SORBIAN](#LOWER-SORBIAN) | Idioma: sorabo inferior |
| [LULE_SAMI_NORWAY](#LULE-SAMI-NORWAY) | Idioma: sami lule (Noruega) |
| [LULE_SAMI_SWEDEN](#LULE-SAMI-SWEDEN) | Idioma: sami lule (Suecia) |
| [LUXEMBOUGISH](#LUXEMBOUGISH) | Idioma: luxemburgués |
| [MACEDONIAN](#MACEDONIAN) | Idioma: macedonio |
| [MALAYALAM](#MALAYALAM) | Idioma: malayalam |
| [MALAY_BRUNEI_DARUSSALAM](#MALAY-BRUNEI-DARUSSALAM) | Idioma: malayo (Brunéi Darussalam) |
| [MALAY_MALAYSIA](#MALAY-MALAYSIA) | Idioma: Malay (Malaysia) |
| [MALTESE](#MALTESE) | Idioma: Maltese |
| [MANIPURI](#MANIPURI) | Idioma: Manipuri |
| [MAORI](#MAORI) | Idioma: Maori |
| [MAPUDUNGUN_CHILE](#MAPUDUNGUN-CHILE) | Idioma: Mapudungun (Chile) |
| [MARATHI](#MARATHI) | Idioma: Marathi |
| [MOHAWK](#MOHAWK) | Idioma: Mohawk |
| [MONGOLIAN_CYRILLIC](#MONGOLIAN-CYRILLIC) | Idioma: Mongolian (Cyrillic) |
| [MONGOLIAN_MONGOLIAN](#MONGOLIAN-MONGOLIAN) | Idioma: Mongolian (Mongolian) |
| [NEPALI](#NEPALI) | Idioma: Nepali |
| [NORTHERN_SAMI_FINLAND](#NORTHERN-SAMI-FINLAND) | Idioma: Northern Sami (Finland) |
| [NORTHERN_SAMI_NORWAY](#NORTHERN-SAMI-NORWAY) | Idioma: Northern Sami (Norway) |
| [NORTHERN_SAMI_SWEDEN](#NORTHERN-SAMI-SWEDEN) | Idioma: Northern Sami (Sweden) |
| [NORWEGIAN_BOKMAL](#NORWEGIAN-BOKMAL) | Idioma: Norwegian Bokmal |
| [NORWEGIAN_NYNORSK](#NORWEGIAN-NYNORSK) | Idioma: Norwegian Nynorsk |
| [ORIYA](#ORIYA) | Idioma: Oriya |
| [OROMO](#OROMO) | Idioma: Oromo |
| [PAPIAMENTU](#PAPIAMENTU) | Idioma: Papiamentu |
| [PASHTO](#PASHTO) | Idioma: Pashto |
| [PERSIAN](#PERSIAN) | Idioma: Persian |
| [POLISH](#POLISH) | Idioma: Polish |
| [PORTUGUESE_BRAZIL](#PORTUGUESE-BRAZIL) | Idioma: Portuguese (Brazil) |
| [PORTUGUESE_PORTUGAL](#PORTUGUESE-PORTUGAL) | Idioma: Portuguese (Portugal) |
| [PUNJABI_INDIA](#PUNJABI-INDIA) | Idioma: Punjabi (India) |
| [PUNJABI_PAKISTAN](#PUNJABI-PAKISTAN) | Idioma: Punjabi (Pakistan) |
| [QUECHUA_BOLIVIA](#QUECHUA-BOLIVIA) | Idioma: Quechua (Bolivia) |
| [QUECHUA_ECUADOR](#QUECHUA-ECUADOR) | Idioma: Quechua (Ecuador) |
| [QUECHUA_PERU](#QUECHUA-PERU) | Idioma: Quechua (Perú) |
| [ROMANIAN](#ROMANIAN) | Idioma: Rumano |
| [ROMANSH](#ROMANSH) | Idioma: Romanche |
| [RUSSIAN](#RUSSIAN) | Idioma: Ruso |
| [SAKHA](#SAKHA) | Idioma: Sakha |
| [SANSKRIT](#SANSKRIT) | Idioma: Sánscrito |
| [SCOTTISH_GAELIC](#SCOTTISH-GAELIC) | Idioma: Gaélico escocés |
| [SERBIAN_CYRILLIC_BOSNIA_AND_HERZEGOVINA](#SERBIAN-CYRILLIC-BOSNIA-AND-HERZEGOVINA) | Idioma: Serbio (Cirílico, Bosnia y Herzegovina) |
| [SERBIAN_CYRILLIC_SERBIA_AND_MONTENEGRO](#SERBIAN-CYRILLIC-SERBIA-AND-MONTENEGRO) | Idioma: Serbio (Cirílico, Serbia y Montenegro) |
| [SERBIAN_LATIN_BOSNIA_AND_HERZEGOVINA](#SERBIAN-LATIN-BOSNIA-AND-HERZEGOVINA) | Idioma: Serbio (Latín, Bosnia y Herzegovina) |
| [SERBIAN_LATIN_SERBIA_AND_MONTENEGRO](#SERBIAN-LATIN-SERBIA-AND-MONTENEGRO) | Idioma: Serbio (Latín, Serbia y Montenegro) |
| [SINDHI](#SINDHI) | Idioma: Sindhi |
| [SINDHI_DEVANAGARIC](#SINDHI-DEVANAGARIC) | Idioma: Sindhi (Devanagari) |
| [SINHALESE](#SINHALESE) | Idioma: Cingalés |
| [SLOVAK](#SLOVAK) | Idioma: Eslovaco |
| [SLOVENIAN](#SLOVENIAN) | Idioma: Esloveno |
| [SOMALI](#SOMALI) | Idioma: Somalí |
| [SORBIAN](#SORBIAN) | Idioma: Sorbio |
| [SPANISH_ARGENTINA](#SPANISH-ARGENTINA) | Idioma: Español (Argentina) |
| [SPANISH_BOLIVIA](#SPANISH-BOLIVIA) | Idioma: Español (Bolivia) |
| [SPANISH_CHILE](#SPANISH-CHILE) | Idioma: Español (Chile) |
| [SPANISH_COLOMBIA](#SPANISH-COLOMBIA) | Idioma: Español (Colombia) |
| [SPANISH_COSTA_RICA](#SPANISH-COSTA-RICA) | Idioma: Español (Costa Rica) |
| [SPANISH_DOMINICAN_REPUBLIC](#SPANISH-DOMINICAN-REPUBLIC) | Idioma: Español (República Dominicana) |
| [SPANISH_ECUADOR](#SPANISH-ECUADOR) | Idioma: Español (Ecuador) |
| [SPANISH_EL_SALVADOR](#SPANISH-EL-SALVADOR) | Idioma: Español (El Salvador) |
| [SPANISH_GUATEMALA](#SPANISH-GUATEMALA) | Idioma: Español (Guatemala) |
| [SPANISH_HONDURAS](#SPANISH-HONDURAS) | Idioma: Español (Honduras) |
| [SPANISH_MEXICO](#SPANISH-MEXICO) | Idioma: Español (México) |
| [SPANISH_NICARAGUA](#SPANISH-NICARAGUA) | Idioma: Español (Nicaragua) |
| [SPANISH_PANAMA](#SPANISH-PANAMA) | Idioma: Español (Panamá) |
| [SPANISH_PARAGUAY](#SPANISH-PARAGUAY) | Idioma: Español (Paraguay) |
| [SPANISH_PERU](#SPANISH-PERU) | Idioma: Español (Perú) |
| [SPANISH_PUERTO_RICO](#SPANISH-PUERTO-RICO) | Idioma: Español (Puerto Rico) |
| [SPANISH_SPAIN_MODERN_SORT](#SPANISH-SPAIN-MODERN-SORT) | Idioma: Español (España, Orden Moderna) |
| [SPANISH_SPAIN_TRADITIONAL_SORT](#SPANISH-SPAIN-TRADITIONAL-SORT) | Idioma: Español (España, Orden Tradicional) |
| [SPANISH_URUGUAY](#SPANISH-URUGUAY) | Idioma: Español (Uruguay) |
| [SPANISH_VENEZUELA](#SPANISH-VENEZUELA) | Idioma: Español (Venezuela) |
| [SUTU](#SUTU) | Idioma: Sutu |
| [SWEDISH_FINLAND](#SWEDISH-FINLAND) | Idioma: Sueco (Finlandia) |
| [SWEDISH_SWEDEN](#SWEDISH-SWEDEN) | Idioma: Sueco (Suecia) |
| [SYRIAC](#SYRIAC) | Idioma: Siríaco |
| [TAJIK](#TAJIK) | Idioma: Tayiko |
| [TAMAZIGHT](#TAMAZIGHT) | Idioma: Tamazight |
| [TAMAZIGHT_LATIN](#TAMAZIGHT-LATIN) | Idioma: Tamazight (Latín) |
| [TAMIL](#TAMIL) | Idioma: Tamil |
| [TATAR](#TATAR) | Idioma: Tártaro |
| [TELUGU](#TELUGU) | Idioma: Telugú |
| [THAI](#THAI) | Idioma: Tailandés |
| [TIBETAN_BUTAN](#TIBETAN-BUTAN) | Idioma: Tibetano (Bután) |
| [TIBETAN_CHINA](#TIBETAN-CHINA) | Idioma: Tibetano (China) |
| [TIGRIGNA_ERITREA](#TIGRIGNA-ERITREA) | Idioma: Tigrigna (Eritrea) |
| [TIGRIGNA_ETHIOPIA](#TIGRIGNA-ETHIOPIA) | Idioma: Tigrigna (Etiopía) |
| [TSONGA](#TSONGA) | Idioma: Tsonga |
| [TSWANA](#TSWANA) | Idioma: Tswana |
| [TURKISH](#TURKISH) | Idioma: Turco |
| [TURKMEN](#TURKMEN) | Idioma: Turcomano |
| [UKRAINIAN](#UKRAINIAN) | Idioma: Ucraniano |
| [URDU](#URDU) | Idioma: Urdu |
| [UZBEK_CYRILLIC](#UZBEK-CYRILLIC) | Idioma: Uzbek (Cirílico) |
| [UZBEK_LATIN](#UZBEK-LATIN) | Idioma: Uzbek (Latín) |
| [VENDA](#VENDA) | Idioma: Venda |
| [VIETNAMESE](#VIETNAMESE) | Idioma: Vietnamita |
| [WELSH](#WELSH) | Idioma: Galés |
| [YI](#YI) | Idioma: Yi |
| [YIDDISH](#YIDDISH) | Idioma: Yidis |
| [YORUBA](#YORUBA) | Idioma: Yoruba |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String editingLanguageName)](#fromName-java.lang.String) |  |
| [getName(int editingLanguage)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int editingLanguage)](#toString-int) |  |
### AFRIKAANS {#AFRIKAANS}
```
public static int AFRIKAANS
```


Idioma: Afrikaans

### ALBANIAN {#ALBANIAN}
```
public static int ALBANIAN
```


Idioma: Albanés

### ALSATIAN {#ALSATIAN}
```
public static int ALSATIAN
```


Idioma: Alsaciano

### AMHARIC {#AMHARIC}
```
public static int AMHARIC
```


Idioma: Amhárico

### ARABIC_ALGERIA {#ARABIC-ALGERIA}
```
public static int ARABIC_ALGERIA
```


Idioma: Árabe (Argelia)

### ARABIC_BAHRAIN {#ARABIC-BAHRAIN}
```
public static int ARABIC_BAHRAIN
```


Idioma: Árabe (Baréin)

### ARABIC_EGYPT {#ARABIC-EGYPT}
```
public static int ARABIC_EGYPT
```


Idioma: Árabe (Egipto)

### ARABIC_IRAQ {#ARABIC-IRAQ}
```
public static int ARABIC_IRAQ
```


Idioma: Árabe (Irak)

### ARABIC_JORDAN {#ARABIC-JORDAN}
```
public static int ARABIC_JORDAN
```


Idioma: Árabe (Jordania)

### ARABIC_KUWAIT {#ARABIC-KUWAIT}
```
public static int ARABIC_KUWAIT
```


Idioma: Árabe (Kuwait)

### ARABIC_LEBANON {#ARABIC-LEBANON}
```
public static int ARABIC_LEBANON
```


Idioma: Árabe (Líbano)

### ARABIC_LIBYA {#ARABIC-LIBYA}
```
public static int ARABIC_LIBYA
```


Idioma: Árabe (Libia)

### ARABIC_MOROCCO {#ARABIC-MOROCCO}
```
public static int ARABIC_MOROCCO
```


Idioma: Árabe (Marruecos)

### ARABIC_OMAN {#ARABIC-OMAN}
```
public static int ARABIC_OMAN
```


Idioma: Árabe (Omán)

### ARABIC_QATAR {#ARABIC-QATAR}
```
public static int ARABIC_QATAR
```


Idioma: Árabe (Catar)

### ARABIC_SAUDI_ARABIA {#ARABIC-SAUDI-ARABIA}
```
public static int ARABIC_SAUDI_ARABIA
```


Idioma: Árabe (Arabia Saudita)

### ARABIC_SYRIA {#ARABIC-SYRIA}
```
public static int ARABIC_SYRIA
```


Idioma: Árabe (Siria)

### ARABIC_TUNISIA {#ARABIC-TUNISIA}
```
public static int ARABIC_TUNISIA
```


Idioma: Árabe (Túnez)

### ARABIC_UAE {#ARABIC-UAE}
```
public static int ARABIC_UAE
```


Idioma: Árabe (Emiratos Árabes Unidos)

### ARABIC_YEMEN {#ARABIC-YEMEN}
```
public static int ARABIC_YEMEN
```


Idioma: Árabe (Yemen)

### ARMENIAN {#ARMENIAN}
```
public static int ARMENIAN
```


Idioma: Armenio

### ASSAMESE {#ASSAMESE}
```
public static int ASSAMESE
```


Idioma: Asamés

### AZERBAIJANI_CYRILLIC {#AZERBAIJANI-CYRILLIC}
```
public static int AZERBAIJANI_CYRILLIC
```


Idioma: Azerbaiyano (Cirílico)

### AZERBAIJANI_LATIN {#AZERBAIJANI-LATIN}
```
public static int AZERBAIJANI_LATIN
```


Idioma: Azerbaiyano (Latín)

### BANGLA_BANGLADESH {#BANGLA-BANGLADESH}
```
public static int BANGLA_BANGLADESH
```


Idioma: Bengalí (Bangladés)

### BANGLA_INDIA {#BANGLA-INDIA}
```
public static int BANGLA_INDIA
```


Idioma: Bengalí (India)

### BASHKIR {#BASHKIR}
```
public static int BASHKIR
```


Idioma: Bashkir

### BASQUE {#BASQUE}
```
public static int BASQUE
```


Idioma: Vasco

### BELARUSIAN {#BELARUSIAN}
```
public static int BELARUSIAN
```


Idioma: Bielorruso

### BOSNIAN_CYRILLIC {#BOSNIAN-CYRILLIC}
```
public static int BOSNIAN_CYRILLIC
```


Idioma: Bosnio (Cirílico)

### BOSNIAN_LATIN {#BOSNIAN-LATIN}
```
public static int BOSNIAN_LATIN
```


Idioma: Bosnio (Latín)

### BRETON {#BRETON}
```
public static int BRETON
```


Idioma: Bretón

### BULGARIAN {#BULGARIAN}
```
public static int BULGARIAN
```


Idioma: Búlgaro

### BURMESE {#BURMESE}
```
public static int BURMESE
```


Idioma: Birmano

### CATALAN {#CATALAN}
```
public static int CATALAN
```


Idioma: Catalán

### CENTRAL_KURDISH_IRAQ {#CENTRAL-KURDISH-IRAQ}
```
public static int CENTRAL_KURDISH_IRAQ
```


Idioma: Kurdo central (Irak)

### CHEROKEE {#CHEROKEE}
```
public static int CHEROKEE
```


Idioma: Cherokee

### CHINESE_HONG_KONG {#CHINESE-HONG-KONG}
```
public static int CHINESE_HONG_KONG
```


Idioma: Chino (Hong Kong)

### CHINESE_MACAO {#CHINESE-MACAO}
```
public static int CHINESE_MACAO
```


Idioma: Chino (Macao)

### CHINESE_PRC {#CHINESE-PRC}
```
public static int CHINESE_PRC
```


Idioma: Chino (RPC)

### CHINESE_SINGAPORE {#CHINESE-SINGAPORE}
```
public static int CHINESE_SINGAPORE
```


Idioma: Chino (Singapur)

### CHINESE_TAIWAN {#CHINESE-TAIWAN}
```
public static int CHINESE_TAIWAN
```


Idioma: Chino (Taiwán)

### CORSICAN {#CORSICAN}
```
public static int CORSICAN
```


Idioma: Corso

### CROATIAN {#CROATIAN}
```
public static int CROATIAN
```


Idioma: Croata

### CROATIAN_BOZNIA_AND_HERZEGOVINA {#CROATIAN-BOZNIA-AND-HERZEGOVINA}
```
public static int CROATIAN_BOZNIA_AND_HERZEGOVINA
```


Idioma: Croata (Bosnia y Herzegovina)

### CZECH {#CZECH}
```
public static int CZECH
```


Idioma: Checo

### DANISH {#DANISH}
```
public static int DANISH
```


Idioma: Danés

### DIVEHI {#DIVEHI}
```
public static int DIVEHI
```


Idioma: Divehi

### DUTCH_BELGIUM {#DUTCH-BELGIUM}
```
public static int DUTCH_BELGIUM
```


Idioma: Holandés (Bélgica)

### DUTCH_NETHERLANDS {#DUTCH-NETHERLANDS}
```
public static int DUTCH_NETHERLANDS
```


Idioma: Holandés (Países Bajos)

### EDO {#EDO}
```
public static int EDO
```


Idioma: Edo

### ENGLISH_AUSTRALIA {#ENGLISH-AUSTRALIA}
```
public static int ENGLISH_AUSTRALIA
```


Idioma: Inglés (Australia)

### ENGLISH_BELIZE {#ENGLISH-BELIZE}
```
public static int ENGLISH_BELIZE
```


Idioma: Inglés (Belice)

### ENGLISH_CANADA {#ENGLISH-CANADA}
```
public static int ENGLISH_CANADA
```


Idioma: Inglés (Canadá)

### ENGLISH_CARIBBEAN {#ENGLISH-CARIBBEAN}
```
public static int ENGLISH_CARIBBEAN
```


Idioma: Inglés (Caribe)

### ENGLISH_HONG_KONG {#ENGLISH-HONG-KONG}
```
public static int ENGLISH_HONG_KONG
```


Idioma: Inglés (Hong Kong)

### ENGLISH_INDIA {#ENGLISH-INDIA}
```
public static int ENGLISH_INDIA
```


Idioma: Inglés (India)

### ENGLISH_INDONESIA {#ENGLISH-INDONESIA}
```
public static int ENGLISH_INDONESIA
```


Idioma: Inglés (Indonesia)

### ENGLISH_IRELAND {#ENGLISH-IRELAND}
```
public static int ENGLISH_IRELAND
```


Idioma: Inglés (Irlanda)

### ENGLISH_JAMAICA {#ENGLISH-JAMAICA}
```
public static int ENGLISH_JAMAICA
```


Idioma: Inglés (Jamaica)

### ENGLISH_MALAYSIA {#ENGLISH-MALAYSIA}
```
public static int ENGLISH_MALAYSIA
```


Idioma: Inglés (Malasia)

### ENGLISH_NEW_ZEALAND {#ENGLISH-NEW-ZEALAND}
```
public static int ENGLISH_NEW_ZEALAND
```


Idioma: Inglés (Nueva Zelanda)

### ENGLISH_PHILIPPINES {#ENGLISH-PHILIPPINES}
```
public static int ENGLISH_PHILIPPINES
```


Idioma: Inglés (Filipinas)

### ENGLISH_SINGAPORE {#ENGLISH-SINGAPORE}
```
public static int ENGLISH_SINGAPORE
```


Idioma: Inglés (Singapur)

### ENGLISH_SOUTH_AFRICA {#ENGLISH-SOUTH-AFRICA}
```
public static int ENGLISH_SOUTH_AFRICA
```


Idioma: Inglés (Sudáfrica)

### ENGLISH_TRINIDAD_AND_TOBAGO {#ENGLISH-TRINIDAD-AND-TOBAGO}
```
public static int ENGLISH_TRINIDAD_AND_TOBAGO
```


Idioma: Inglés (Trinidad y Tobago)

### ENGLISH_UK {#ENGLISH-UK}
```
public static int ENGLISH_UK
```


Idioma: Inglés (Reino Unido)

### ENGLISH_US {#ENGLISH-US}
```
public static int ENGLISH_US
```


Idioma: Inglés (EE. UU.)

### ENGLISH_ZIMBABWE {#ENGLISH-ZIMBABWE}
```
public static int ENGLISH_ZIMBABWE
```


Idioma: Inglés (Zimbabue)

### ESTONIAN {#ESTONIAN}
```
public static int ESTONIAN
```


Estonio

### FAEROESE {#FAEROESE}
```
public static int FAEROESE
```


Feroés

### FILIPINO {#FILIPINO}
```
public static int FILIPINO
```


Filipino

### FINNISH {#FINNISH}
```
public static int FINNISH
```


Finlandés

### FRENCH_BELGIUM {#FRENCH-BELGIUM}
```
public static int FRENCH_BELGIUM
```


Francés (Bélgica)

### FRENCH_CANADA {#FRENCH-CANADA}
```
public static int FRENCH_CANADA
```


Francés (Canadá)

### FRENCH_FRANCE {#FRENCH-FRANCE}
```
public static int FRENCH_FRANCE
```


Francés (Francia)

### FRENCH_LUXEMBOURG {#FRENCH-LUXEMBOURG}
```
public static int FRENCH_LUXEMBOURG
```


Francés (Luxemburgo)

### FRENCH_MONACO {#FRENCH-MONACO}
```
public static int FRENCH_MONACO
```


Francés (Mónaco)

### FRENCH_SWITZERLAND {#FRENCH-SWITZERLAND}
```
public static int FRENCH_SWITZERLAND
```


Francés (Suiza)

### FRISIAN {#FRISIAN}
```
public static int FRISIAN
```


Frisón

### FULAH_LATIN_SENEGAL {#FULAH-LATIN-SENEGAL}
```
public static int FULAH_LATIN_SENEGAL
```


Fulah (Latín, Senegal)

### FULAH_NIGERIA {#FULAH-NIGERIA}
```
public static int FULAH_NIGERIA
```


Fulah (Nigeria)

### GALICIAN {#GALICIAN}
```
public static int GALICIAN
```


Gallego

### GEORGIAN {#GEORGIAN}
```
public static int GEORGIAN
```


Idioma: georgiano

### GERMAN_AUSTRIA {#GERMAN-AUSTRIA}
```
public static int GERMAN_AUSTRIA
```


Idioma: alemán (Austria)

### GERMAN_GERMANY {#GERMAN-GERMANY}
```
public static int GERMAN_GERMANY
```


Idioma: alemán (Alemania)

### GERMAN_LIECHTENSTEIN {#GERMAN-LIECHTENSTEIN}
```
public static int GERMAN_LIECHTENSTEIN
```


Idioma: alemán (Liechtenstein)

### GERMAN_LUXEMBOURG {#GERMAN-LUXEMBOURG}
```
public static int GERMAN_LUXEMBOURG
```


Idioma: alemán (Luxemburgo)

### GERMAN_SWITZERLAND {#GERMAN-SWITZERLAND}
```
public static int GERMAN_SWITZERLAND
```


Idioma: alemán (Suiza)

### GREEK {#GREEK}
```
public static int GREEK
```


Idioma: griego

### GREENLANDIC {#GREENLANDIC}
```
public static int GREENLANDIC
```


Idioma: groenlandés

### GUARANI {#GUARANI}
```
public static int GUARANI
```


Idioma: guaraní

### GUJARATI {#GUJARATI}
```
public static int GUJARATI
```


Idioma: gujarati

### HAUSA {#HAUSA}
```
public static int HAUSA
```


Idioma: hausa

### HAWAIIAN {#HAWAIIAN}
```
public static int HAWAIIAN
```


Idioma: hawaiano

### HEBREW {#HEBREW}
```
public static int HEBREW
```


Idioma: hebreo

### HINDI {#HINDI}
```
public static int HINDI
```


Idioma: hindi

### HUNGARIAN {#HUNGARIAN}
```
public static int HUNGARIAN
```


Idioma: húngaro

### ICELANDIC {#ICELANDIC}
```
public static int ICELANDIC
```


Idioma: islandés

### IGBO {#IGBO}
```
public static int IGBO
```


Idioma: igbo

### INARI_SAMI_FINLAND {#INARI-SAMI-FINLAND}
```
public static int INARI_SAMI_FINLAND
```


Idioma: Inari Sami (Finlandia)

### INDONESIAN {#INDONESIAN}
```
public static int INDONESIAN
```


Idioma: indonesio

### INUKTITUT_LATIN {#INUKTITUT-LATIN}
```
public static int INUKTITUT_LATIN
```


Idioma: inuktitut (Latín)

### INUKTITUT_SYLLABICS {#INUKTITUT-SYLLABICS}
```
public static int INUKTITUT_SYLLABICS
```


Idioma: inuktitut (Silábico)

### IRISH {#IRISH}
```
public static int IRISH
```


Idioma: irlandés

### ISI_XHOSA {#ISI-XHOSA}
```
public static int ISI_XHOSA
```


Idioma: isiXhosa

### ISI_ZULU {#ISI-ZULU}
```
public static int ISI_ZULU
```


Idioma: isiZulu

### ITALIAN_ITALY {#ITALIAN-ITALY}
```
public static int ITALIAN_ITALY
```


Idioma: italiano (Italia)

### ITALIAN_SWITZERLAND {#ITALIAN-SWITZERLAND}
```
public static int ITALIAN_SWITZERLAND
```


Idioma: italiano (Suiza)

### JAPANESE {#JAPANESE}
```
public static int JAPANESE
```


Idioma: japonés

### KANNADA {#KANNADA}
```
public static int KANNADA
```


Idioma: kannada

### KANURI {#KANURI}
```
public static int KANURI
```


Idioma: kanuri

### KASHMIRI {#KASHMIRI}
```
public static int KASHMIRI
```


Idioma: cachemiro

### KASHMIRI_ARABIC {#KASHMIRI-ARABIC}
```
public static int KASHMIRI_ARABIC
```


Idioma: cachemiro (árabe)

### KAZAKH {#KAZAKH}
```
public static int KAZAKH
```


Idioma: kazajo

### KHMER {#KHMER}
```
public static int KHMER
```


Idioma: jemer

### KICHE {#KICHE}
```
public static int KICHE
```


Idioma: k'iche'

### KINYARWANDA {#KINYARWANDA}
```
public static int KINYARWANDA
```


Idioma: kinyarwanda

### KISWAHILI {#KISWAHILI}
```
public static int KISWAHILI
```


Idioma: kiswahili

### KONKANI {#KONKANI}
```
public static int KONKANI
```


Idioma: konkani

### KOREAN {#KOREAN}
```
public static int KOREAN
```


Idioma: coreano

### KYRGYZ {#KYRGYZ}
```
public static int KYRGYZ
```


Idioma: kirguís

### LAO {#LAO}
```
public static int LAO
```


Idioma: lao

### LATIN {#LATIN}
```
public static int LATIN
```


Idioma: latín

### LATVIAN {#LATVIAN}
```
public static int LATVIAN
```


Idioma: letón

### LITHUANIAN {#LITHUANIAN}
```
public static int LITHUANIAN
```


Idioma: lituano

### LOWER_SORBIAN {#LOWER-SORBIAN}
```
public static int LOWER_SORBIAN
```


Idioma: sorabo inferior

### LULE_SAMI_NORWAY {#LULE-SAMI-NORWAY}
```
public static int LULE_SAMI_NORWAY
```


Idioma: sami lule (Noruega)

### LULE_SAMI_SWEDEN {#LULE-SAMI-SWEDEN}
```
public static int LULE_SAMI_SWEDEN
```


Idioma: sami lule (Suecia)

### LUXEMBOUGISH {#LUXEMBOUGISH}
```
public static int LUXEMBOUGISH
```


Idioma: luxemburgués

### MACEDONIAN {#MACEDONIAN}
```
public static int MACEDONIAN
```


Idioma: macedonio

### MALAYALAM {#MALAYALAM}
```
public static int MALAYALAM
```


Idioma: malayalam

### MALAY_BRUNEI_DARUSSALAM {#MALAY-BRUNEI-DARUSSALAM}
```
public static int MALAY_BRUNEI_DARUSSALAM
```


Idioma: malayo (Brunéi Darussalam)

### MALAY_MALAYSIA {#MALAY-MALAYSIA}
```
public static int MALAY_MALAYSIA
```


Idioma: Malay (Malaysia)

### MALTESE {#MALTESE}
```
public static int MALTESE
```


Idioma: Maltese

### MANIPURI {#MANIPURI}
```
public static int MANIPURI
```


Idioma: Manipuri

### MAORI {#MAORI}
```
public static int MAORI
```


Idioma: Maori

### MAPUDUNGUN_CHILE {#MAPUDUNGUN-CHILE}
```
public static int MAPUDUNGUN_CHILE
```


Idioma: Mapudungun (Chile)

### MARATHI {#MARATHI}
```
public static int MARATHI
```


Idioma: Marathi

### MOHAWK {#MOHAWK}
```
public static int MOHAWK
```


Idioma: Mohawk

### MONGOLIAN_CYRILLIC {#MONGOLIAN-CYRILLIC}
```
public static int MONGOLIAN_CYRILLIC
```


Idioma: Mongolian (Cyrillic)

### MONGOLIAN_MONGOLIAN {#MONGOLIAN-MONGOLIAN}
```
public static int MONGOLIAN_MONGOLIAN
```


Idioma: Mongolian (Mongolian)

### NEPALI {#NEPALI}
```
public static int NEPALI
```


Idioma: Nepali

### NORTHERN_SAMI_FINLAND {#NORTHERN-SAMI-FINLAND}
```
public static int NORTHERN_SAMI_FINLAND
```


Idioma: Northern Sami (Finland)

### NORTHERN_SAMI_NORWAY {#NORTHERN-SAMI-NORWAY}
```
public static int NORTHERN_SAMI_NORWAY
```


Idioma: Northern Sami (Norway)

### NORTHERN_SAMI_SWEDEN {#NORTHERN-SAMI-SWEDEN}
```
public static int NORTHERN_SAMI_SWEDEN
```


Idioma: Northern Sami (Sweden)

### NORWEGIAN_BOKMAL {#NORWEGIAN-BOKMAL}
```
public static int NORWEGIAN_BOKMAL
```


Idioma: Norwegian Bokmal

### NORWEGIAN_NYNORSK {#NORWEGIAN-NYNORSK}
```
public static int NORWEGIAN_NYNORSK
```


Idioma: Norwegian Nynorsk

### ORIYA {#ORIYA}
```
public static int ORIYA
```


Idioma: Oriya

### OROMO {#OROMO}
```
public static int OROMO
```


Idioma: Oromo

### PAPIAMENTU {#PAPIAMENTU}
```
public static int PAPIAMENTU
```


Idioma: Papiamentu

### PASHTO {#PASHTO}
```
public static int PASHTO
```


Idioma: Pashto

### PERSIAN {#PERSIAN}
```
public static int PERSIAN
```


Idioma: Persian

### POLISH {#POLISH}
```
public static int POLISH
```


Idioma: Polish

### PORTUGUESE_BRAZIL {#PORTUGUESE-BRAZIL}
```
public static int PORTUGUESE_BRAZIL
```


Idioma: Portuguese (Brazil)

### PORTUGUESE_PORTUGAL {#PORTUGUESE-PORTUGAL}
```
public static int PORTUGUESE_PORTUGAL
```


Idioma: Portuguese (Portugal)

### PUNJABI_INDIA {#PUNJABI-INDIA}
```
public static int PUNJABI_INDIA
```


Idioma: Punjabi (India)

### PUNJABI_PAKISTAN {#PUNJABI-PAKISTAN}
```
public static int PUNJABI_PAKISTAN
```


Idioma: Punjabi (Pakistan)

### QUECHUA_BOLIVIA {#QUECHUA-BOLIVIA}
```
public static int QUECHUA_BOLIVIA
```


Idioma: Quechua (Bolivia)

### QUECHUA_ECUADOR {#QUECHUA-ECUADOR}
```
public static int QUECHUA_ECUADOR
```


Idioma: Quechua (Ecuador)

### QUECHUA_PERU {#QUECHUA-PERU}
```
public static int QUECHUA_PERU
```


Idioma: Quechua (Perú)

### ROMANIAN {#ROMANIAN}
```
public static int ROMANIAN
```


Idioma: Rumano

### ROMANSH {#ROMANSH}
```
public static int ROMANSH
```


Idioma: Romanche

### RUSSIAN {#RUSSIAN}
```
public static int RUSSIAN
```


Idioma: Ruso

### SAKHA {#SAKHA}
```
public static int SAKHA
```


Idioma: Sakha

### SANSKRIT {#SANSKRIT}
```
public static int SANSKRIT
```


Idioma: Sánscrito

### SCOTTISH_GAELIC {#SCOTTISH-GAELIC}
```
public static int SCOTTISH_GAELIC
```


Idioma: Gaélico escocés

### SERBIAN_CYRILLIC_BOSNIA_AND_HERZEGOVINA {#SERBIAN-CYRILLIC-BOSNIA-AND-HERZEGOVINA}
```
public static int SERBIAN_CYRILLIC_BOSNIA_AND_HERZEGOVINA
```


Idioma: Serbio (Cirílico, Bosnia y Herzegovina)

### SERBIAN_CYRILLIC_SERBIA_AND_MONTENEGRO {#SERBIAN-CYRILLIC-SERBIA-AND-MONTENEGRO}
```
public static int SERBIAN_CYRILLIC_SERBIA_AND_MONTENEGRO
```


Idioma: Serbio (Cirílico, Serbia y Montenegro)

### SERBIAN_LATIN_BOSNIA_AND_HERZEGOVINA {#SERBIAN-LATIN-BOSNIA-AND-HERZEGOVINA}
```
public static int SERBIAN_LATIN_BOSNIA_AND_HERZEGOVINA
```


Idioma: Serbio (Latín, Bosnia y Herzegovina)

### SERBIAN_LATIN_SERBIA_AND_MONTENEGRO {#SERBIAN-LATIN-SERBIA-AND-MONTENEGRO}
```
public static int SERBIAN_LATIN_SERBIA_AND_MONTENEGRO
```


Idioma: Serbio (Latín, Serbia y Montenegro)

### SINDHI {#SINDHI}
```
public static int SINDHI
```


Idioma: Sindhi

### SINDHI_DEVANAGARIC {#SINDHI-DEVANAGARIC}
```
public static int SINDHI_DEVANAGARIC
```


Idioma: Sindhi (Devanagari)

### SINHALESE {#SINHALESE}
```
public static int SINHALESE
```


Idioma: Cingalés

### SLOVAK {#SLOVAK}
```
public static int SLOVAK
```


Idioma: Eslovaco

### SLOVENIAN {#SLOVENIAN}
```
public static int SLOVENIAN
```


Idioma: Esloveno

### SOMALI {#SOMALI}
```
public static int SOMALI
```


Idioma: Somalí

### SORBIAN {#SORBIAN}
```
public static int SORBIAN
```


Idioma: Sorbio

### SPANISH_ARGENTINA {#SPANISH-ARGENTINA}
```
public static int SPANISH_ARGENTINA
```


Idioma: Español (Argentina)

### SPANISH_BOLIVIA {#SPANISH-BOLIVIA}
```
public static int SPANISH_BOLIVIA
```


Idioma: Español (Bolivia)

### SPANISH_CHILE {#SPANISH-CHILE}
```
public static int SPANISH_CHILE
```


Idioma: Español (Chile)

### SPANISH_COLOMBIA {#SPANISH-COLOMBIA}
```
public static int SPANISH_COLOMBIA
```


Idioma: Español (Colombia)

### SPANISH_COSTA_RICA {#SPANISH-COSTA-RICA}
```
public static int SPANISH_COSTA_RICA
```


Idioma: Español (Costa Rica)

### SPANISH_DOMINICAN_REPUBLIC {#SPANISH-DOMINICAN-REPUBLIC}
```
public static int SPANISH_DOMINICAN_REPUBLIC
```


Idioma: Español (República Dominicana)

### SPANISH_ECUADOR {#SPANISH-ECUADOR}
```
public static int SPANISH_ECUADOR
```


Idioma: Español (Ecuador)

### SPANISH_EL_SALVADOR {#SPANISH-EL-SALVADOR}
```
public static int SPANISH_EL_SALVADOR
```


Idioma: Español (El Salvador)

### SPANISH_GUATEMALA {#SPANISH-GUATEMALA}
```
public static int SPANISH_GUATEMALA
```


Idioma: Español (Guatemala)

### SPANISH_HONDURAS {#SPANISH-HONDURAS}
```
public static int SPANISH_HONDURAS
```


Idioma: Español (Honduras)

### SPANISH_MEXICO {#SPANISH-MEXICO}
```
public static int SPANISH_MEXICO
```


Idioma: Español (México)

### SPANISH_NICARAGUA {#SPANISH-NICARAGUA}
```
public static int SPANISH_NICARAGUA
```


Idioma: Español (Nicaragua)

### SPANISH_PANAMA {#SPANISH-PANAMA}
```
public static int SPANISH_PANAMA
```


Idioma: Español (Panamá)

### SPANISH_PARAGUAY {#SPANISH-PARAGUAY}
```
public static int SPANISH_PARAGUAY
```


Idioma: Español (Paraguay)

### SPANISH_PERU {#SPANISH-PERU}
```
public static int SPANISH_PERU
```


Idioma: Español (Perú)

### SPANISH_PUERTO_RICO {#SPANISH-PUERTO-RICO}
```
public static int SPANISH_PUERTO_RICO
```


Idioma: Español (Puerto Rico)

### SPANISH_SPAIN_MODERN_SORT {#SPANISH-SPAIN-MODERN-SORT}
```
public static int SPANISH_SPAIN_MODERN_SORT
```


Idioma: Español (España, Orden Moderna)

### SPANISH_SPAIN_TRADITIONAL_SORT {#SPANISH-SPAIN-TRADITIONAL-SORT}
```
public static int SPANISH_SPAIN_TRADITIONAL_SORT
```


Idioma: Español (España, Orden Tradicional)

### SPANISH_URUGUAY {#SPANISH-URUGUAY}
```
public static int SPANISH_URUGUAY
```


Idioma: Español (Uruguay)

### SPANISH_VENEZUELA {#SPANISH-VENEZUELA}
```
public static int SPANISH_VENEZUELA
```


Idioma: Español (Venezuela)

### SUTU {#SUTU}
```
public static int SUTU
```


Idioma: Sutu

### SWEDISH_FINLAND {#SWEDISH-FINLAND}
```
public static int SWEDISH_FINLAND
```


Idioma: Sueco (Finlandia)

### SWEDISH_SWEDEN {#SWEDISH-SWEDEN}
```
public static int SWEDISH_SWEDEN
```


Idioma: Sueco (Suecia)

### SYRIAC {#SYRIAC}
```
public static int SYRIAC
```


Idioma: Siríaco

### TAJIK {#TAJIK}
```
public static int TAJIK
```


Idioma: Tayiko

### TAMAZIGHT {#TAMAZIGHT}
```
public static int TAMAZIGHT
```


Idioma: Tamazight

### TAMAZIGHT_LATIN {#TAMAZIGHT-LATIN}
```
public static int TAMAZIGHT_LATIN
```


Idioma: Tamazight (Latín)

### TAMIL {#TAMIL}
```
public static int TAMIL
```


Idioma: Tamil

### TATAR {#TATAR}
```
public static int TATAR
```


Idioma: Tártaro

### TELUGU {#TELUGU}
```
public static int TELUGU
```


Idioma: Telugú

### THAI {#THAI}
```
public static int THAI
```


Idioma: Tailandés

### TIBETAN_BUTAN {#TIBETAN-BUTAN}
```
public static int TIBETAN_BUTAN
```


Idioma: Tibetano (Bután)

### TIBETAN_CHINA {#TIBETAN-CHINA}
```
public static int TIBETAN_CHINA
```


Idioma: Tibetano (China)

### TIGRIGNA_ERITREA {#TIGRIGNA-ERITREA}
```
public static int TIGRIGNA_ERITREA
```


Idioma: Tigrigna (Eritrea)

### TIGRIGNA_ETHIOPIA {#TIGRIGNA-ETHIOPIA}
```
public static int TIGRIGNA_ETHIOPIA
```


Idioma: Tigrigna (Etiopía)

### TSONGA {#TSONGA}
```
public static int TSONGA
```


Idioma: Tsonga

### TSWANA {#TSWANA}
```
public static int TSWANA
```


Idioma: Tswana

### TURKISH {#TURKISH}
```
public static int TURKISH
```


Idioma: Turco

### TURKMEN {#TURKMEN}
```
public static int TURKMEN
```


Idioma: Turcomano

### UKRAINIAN {#UKRAINIAN}
```
public static int UKRAINIAN
```


Idioma: Ucraniano

### URDU {#URDU}
```
public static int URDU
```


Idioma: Urdu

### UZBEK_CYRILLIC {#UZBEK-CYRILLIC}
```
public static int UZBEK_CYRILLIC
```


Idioma: Uzbek (Cirílico)

### UZBEK_LATIN {#UZBEK-LATIN}
```
public static int UZBEK_LATIN
```


Idioma: Uzbek (Latín)

### VENDA {#VENDA}
```
public static int VENDA
```


Idioma: Venda

### VIETNAMESE {#VIETNAMESE}
```
public static int VIETNAMESE
```


Idioma: Vietnamita

### WELSH {#WELSH}
```
public static int WELSH
```


Idioma: Galés

### YI {#YI}
```
public static int YI
```


Idioma: Yi

### YIDDISH {#YIDDISH}
```
public static int YIDDISH
```


Idioma: Yidis

### YORUBA {#YORUBA}
```
public static int YORUBA
```


Idioma: Yoruba

### length {#length}
```
public static int length
```


### fromName(String editingLanguageName) {#fromName-java.lang.String}
```
public static int fromName(String editingLanguageName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| editingLanguageName | java.lang.String |  |

**Returns:**
int
### getName(int editingLanguage) {#getName-int}
```
public static String getName(int editingLanguage)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| editingLanguage | int |  |

**Returns:**
java.lang.String
