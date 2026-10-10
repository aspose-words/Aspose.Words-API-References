---
title: "EditingLanguage"
linktitle: "EditingLanguage"
second_title: "Aspose.Words Java için"
description: "Java'da düzenleme dilini belirtir."
type: docs
weight: 182
url: /tr/java/com.aspose.words/editinglanguage/
---

**Inheritance:**
java.lang.Object
```
public class EditingLanguage
```

Düzenleme dilini belirtir.

 **Examples:** 

Bir belgeyi yüklerken dil tercihlerini nasıl uygulayacağınızı gösterir.

```

 LoadOptions loadOptions = new LoadOptions();
 loadOptions.getLanguagePreferences().addEditingLanguage(EditingLanguage.JAPANESE);

 Document doc = new Document(getMyDir() + "No default editing language.docx", loadOptions);

 int localeIdFarEast = doc.getStyles().getDefaultFont().getLocaleIdFarEast();
 System.out.println(localeIdFarEast == EditingLanguage.JAPANESE
         ? "The document either has no any FarEast language set in defaults or it was set to Japanese originally."
         : "The document default FarEast language was set to another than Japanese language originally, so it is not overridden.");
 
```
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [AFRIKAANS](#AFRIKAANS) | Dil: Afrikaans |
| [ALBANIAN](#ALBANIAN) | Dil: Albanian |
| [ALSATIAN](#ALSATIAN) | Dil: Alsatian |
| [AMHARIC](#AMHARIC) | Dil: Amharic |
| [ARABIC_ALGERIA](#ARABIC-ALGERIA) | Dil: Arabic (Algeria) |
| [ARABIC_BAHRAIN](#ARABIC-BAHRAIN) | Dil: Arabic (Bahrain) |
| [ARABIC_EGYPT](#ARABIC-EGYPT) | Dil: Arabic (Egypt) |
| [ARABIC_IRAQ](#ARABIC-IRAQ) | Dil: Arabic (Iraq) |
| [ARABIC_JORDAN](#ARABIC-JORDAN) | Dil: Arapça (Ürdün) |
| [ARABIC_KUWAIT](#ARABIC-KUWAIT) | Dil: Arapça (Kuveyt) |
| [ARABIC_LEBANON](#ARABIC-LEBANON) | Dil: Arapça (Lübnan) |
| [ARABIC_LIBYA](#ARABIC-LIBYA) | Dil: Arapça (Libya) |
| [ARABIC_MOROCCO](#ARABIC-MOROCCO) | Dil: Arapça (Fas) |
| [ARABIC_OMAN](#ARABIC-OMAN) | Dil: Arapça (Umman) |
| [ARABIC_QATAR](#ARABIC-QATAR) | Dil: Arapça (Katar) |
| [ARABIC_SAUDI_ARABIA](#ARABIC-SAUDI-ARABIA) | Dil: Arapça (Suudi Arabistan) |
| [ARABIC_SYRIA](#ARABIC-SYRIA) | Dil: Arapça (Suriye) |
| [ARABIC_TUNISIA](#ARABIC-TUNISIA) | Dil: Arapça (Tunus) |
| [ARABIC_UAE](#ARABIC-UAE) | Dil: Arapça (Birleşik Arap Emirlikleri) |
| [ARABIC_YEMEN](#ARABIC-YEMEN) | Dil: Arapça (Yemen) |
| [ARMENIAN](#ARMENIAN) | Dil: Ermenice |
| [ASSAMESE](#ASSAMESE) | Dil: Assamca |
| [AZERBAIJANI_CYRILLIC](#AZERBAIJANI-CYRILLIC) | Dil: Azerbaycanca (Kiril) |
| [AZERBAIJANI_LATIN](#AZERBAIJANI-LATIN) | Dil: Azerbaycanca (Latin) |
| [BANGLA_BANGLADESH](#BANGLA-BANGLADESH) | Dil: Bangla (Bangladeş) |
| [BANGLA_INDIA](#BANGLA-INDIA) | Dil: Bangla (Hindistan) |
| [BASHKIR](#BASHKIR) | Dil: Başkurtça |
| [BASQUE](#BASQUE) | Dil: Baskça |
| [BELARUSIAN](#BELARUSIAN) | Dil: Beyaz Rusça |
| [BOSNIAN_CYRILLIC](#BOSNIAN-CYRILLIC) | Dil: Boşnakça (Kiril) |
| [BOSNIAN_LATIN](#BOSNIAN-LATIN) | Dil: Boşnakça (Latin) |
| [BRETON](#BRETON) | Dil: Bretonca |
| [BULGARIAN](#BULGARIAN) | Dil: Bulgarca |
| [BURMESE](#BURMESE) | Dil: Burmese |
| [CATALAN](#CATALAN) | Dil: Catalan |
| [CENTRAL_KURDISH_IRAQ](#CENTRAL-KURDISH-IRAQ) | Dil: Central Kurdish (Iraq) |
| [CHEROKEE](#CHEROKEE) | Dil: Cherokee |
| [CHINESE_HONG_KONG](#CHINESE-HONG-KONG) | Dil: Chinese (Hong Kong) |
| [CHINESE_MACAO](#CHINESE-MACAO) | Dil: Chinese (Macao) |
| [CHINESE_PRC](#CHINESE-PRC) | Dil: Chinese (PRC) |
| [CHINESE_SINGAPORE](#CHINESE-SINGAPORE) | Dil: Chinese (Singapore) |
| [CHINESE_TAIWAN](#CHINESE-TAIWAN) | Dil: Chinese (Taiwan) |
| [CORSICAN](#CORSICAN) | Dil: Corsican |
| [CROATIAN](#CROATIAN) | Dil: Croatian |
| [CROATIAN_BOZNIA_AND_HERZEGOVINA](#CROATIAN-BOZNIA-AND-HERZEGOVINA) | Dil: Croatian (Bosnia and Herzegovina) |
| [CZECH](#CZECH) | Dil: Czech |
| [DANISH](#DANISH) | Dil: Danish |
| [DIVEHI](#DIVEHI) | Dil: Divehi |
| [DUTCH_BELGIUM](#DUTCH-BELGIUM) | Dil: Dutch (Belgium) |
| [DUTCH_NETHERLANDS](#DUTCH-NETHERLANDS) | Dil: Dutch (Netherlands) |
| [EDO](#EDO) | Dil: Edo |
| [ENGLISH_AUSTRALIA](#ENGLISH-AUSTRALIA) | Dil: English (Australia) |
| [ENGLISH_BELIZE](#ENGLISH-BELIZE) | Dil: English (Belize) |
| [ENGLISH_CANADA](#ENGLISH-CANADA) | Dil: English (Canada) |
| [ENGLISH_CARIBBEAN](#ENGLISH-CARIBBEAN) | Dil: English (Caribbean) |
| [ENGLISH_HONG_KONG](#ENGLISH-HONG-KONG) | Dil: English (Hong Kong) |
| [ENGLISH_INDIA](#ENGLISH-INDIA) | Dil: English (India) |
| [ENGLISH_INDONESIA](#ENGLISH-INDONESIA) | Dil: English (Indonesia) |
| [ENGLISH_IRELAND](#ENGLISH-IRELAND) | Dil: İngilizce (İrlanda) |
| [ENGLISH_JAMAICA](#ENGLISH-JAMAICA) | Dil: İngilizce (Jamaika) |
| [ENGLISH_MALAYSIA](#ENGLISH-MALAYSIA) | Dil: İngilizce (Malezya) |
| [ENGLISH_NEW_ZEALAND](#ENGLISH-NEW-ZEALAND) | Dil: İngilizce (Yeni Zelanda) |
| [ENGLISH_PHILIPPINES](#ENGLISH-PHILIPPINES) | Dil: İngilizce (Filipinler) |
| [ENGLISH_SINGAPORE](#ENGLISH-SINGAPORE) | Dil: İngilizce (Singapur) |
| [ENGLISH_SOUTH_AFRICA](#ENGLISH-SOUTH-AFRICA) | Dil: İngilizce (Güney Afrika) |
| [ENGLISH_TRINIDAD_AND_TOBAGO](#ENGLISH-TRINIDAD-AND-TOBAGO) | Dil: İngilizce (Trinidad ve Tobago) |
| [ENGLISH_UK](#ENGLISH-UK) | Dil: İngilizce (Birleşik Krallık) |
| [ENGLISH_US](#ENGLISH-US) | Dil: İngilizce (ABD) |
| [ENGLISH_ZIMBABWE](#ENGLISH-ZIMBABWE) | Dil: İngilizce (Zimbabve) |
| [ESTONIAN](#ESTONIAN) | Dil: Estonca |
| [FAEROESE](#FAEROESE) | Dil: Faroe Dili |
| [FILIPINO](#FILIPINO) | Dil: Filipince |
| [FINNISH](#FINNISH) | Dil: Fince |
| [FRENCH_BELGIUM](#FRENCH-BELGIUM) | Dil: Fransızca (Belçika) |
| [FRENCH_CANADA](#FRENCH-CANADA) | Dil: Fransızca (Kanada) |
| [FRENCH_FRANCE](#FRENCH-FRANCE) | Dil: Fransızca (Fransa) |
| [FRENCH_LUXEMBOURG](#FRENCH-LUXEMBOURG) | Dil: Fransızca (Lüksemburg) |
| [FRENCH_MONACO](#FRENCH-MONACO) | Dil: Fransızca (Monako) |
| [FRENCH_SWITZERLAND](#FRENCH-SWITZERLAND) | Dil: Fransızca (İsviçre) |
| [FRISIAN](#FRISIAN) | Dil: Frizce |
| [FULAH_LATIN_SENEGAL](#FULAH-LATIN-SENEGAL) | Dil: Fulah (Latin, Senegal) |
| [FULAH_NIGERIA](#FULAH-NIGERIA) | Dil: Fulah (Nijerya) |
| [GALICIAN](#GALICIAN) | Dil: Galiçyaca |
| [GEORGIAN](#GEORGIAN) | Dil: Gürcüce |
| [GERMAN_AUSTRIA](#GERMAN-AUSTRIA) | Dil: Almanca (Avusturya) |
| [GERMAN_GERMANY](#GERMAN-GERMANY) | Dil: Almanca (Almanya) |
| [GERMAN_LIECHTENSTEIN](#GERMAN-LIECHTENSTEIN) | Dil: Almanca (Lihtenştayn) |
| [GERMAN_LUXEMBOURG](#GERMAN-LUXEMBOURG) | Dil: Almanca (Lüksemburg) |
| [GERMAN_SWITZERLAND](#GERMAN-SWITZERLAND) | Dil: Almanca (İsviçre) |
| [GREEK](#GREEK) | Dil: Yunanca |
| [GREENLANDIC](#GREENLANDIC) | Dil: Grönlandca |
| [GUARANI](#GUARANI) | Dil: Guarani |
| [GUJARATI](#GUJARATI) | Dil: Gujaratça |
| [HAUSA](#HAUSA) | Dil: Hausa |
| [HAWAIIAN](#HAWAIIAN) | Dil: Hawaiice |
| [HEBREW](#HEBREW) | Dil: İbranice |
| [HINDI](#HINDI) | Dil: Hintçe |
| [HUNGARIAN](#HUNGARIAN) | Dil: Macarca |
| [ICELANDIC](#ICELANDIC) | Dil: İzlandca |
| [IGBO](#IGBO) | Dil: Igbo |
| [INARI_SAMI_FINLAND](#INARI-SAMI-FINLAND) | Dil: Inari Samice (Finlandiya) |
| [INDONESIAN](#INDONESIAN) | Dil: Endonezce |
| [INUKTITUT_LATIN](#INUKTITUT-LATIN) | Dil: İnuktitut (Latin) |
| [INUKTITUT_SYLLABICS](#INUKTITUT-SYLLABICS) | Dil: İnuktitut (Heceleme) |
| [IRISH](#IRISH) | Dil: İrlandaca |
| [ISI_XHOSA](#ISI-XHOSA) | Dil: IsiXhosa |
| [ISI_ZULU](#ISI-ZULU) | Dil: IsiZulu |
| [ITALIAN_ITALY](#ITALIAN-ITALY) | Dil: İtalyanca (İtalya) |
| [ITALIAN_SWITZERLAND](#ITALIAN-SWITZERLAND) | Dil: İtalyanca (İsviçre) |
| [JAPANESE](#JAPANESE) | Dil: Japonca |
| [KANNADA](#KANNADA) | Dil: Kannada |
| [KANURI](#KANURI) | Dil: Kanuri |
| [KASHMIRI](#KASHMIRI) | Dil: Keşmirce |
| [KASHMIRI_ARABIC](#KASHMIRI-ARABIC) | Dil: Keşmirce (Arapça) |
| [KAZAKH](#KAZAKH) | Dil: Kazakça |
| [KHMER](#KHMER) | Dil: Khmer |
| [KICHE](#KICHE) | Dil: Kiche |
| [KINYARWANDA](#KINYARWANDA) | Dil: Kinyarwanda |
| [KISWAHILI](#KISWAHILI) | Dil: Swahili |
| [KONKANI](#KONKANI) | Dil: Konkani |
| [KOREAN](#KOREAN) | Dil: Korece |
| [KYRGYZ](#KYRGYZ) | Dil: Kırgızca |
| [LAO](#LAO) | Dil: Lao |
| [LATIN](#LATIN) | Dil: Latince |
| [LATVIAN](#LATVIAN) | Dil: Letonca |
| [LITHUANIAN](#LITHUANIAN) | Dil: Litvanca |
| [LOWER_SORBIAN](#LOWER-SORBIAN) | Dil: Aşağı Sorbça |
| [LULE_SAMI_NORWAY](#LULE-SAMI-NORWAY) | Dil: Lule Sami (Norveç) |
| [LULE_SAMI_SWEDEN](#LULE-SAMI-SWEDEN) | Dil: Lule Sami (İsveç) |
| [LUXEMBOUGISH](#LUXEMBOUGISH) | Dil: Lüksemburgca |
| [MACEDONIAN](#MACEDONIAN) | Dil: Makedonca |
| [MALAYALAM](#MALAYALAM) | Dil: Malayalam |
| [MALAY_BRUNEI_DARUSSALAM](#MALAY-BRUNEI-DARUSSALAM) | Dil: Malayca (Brunei Darussalam) |
| [MALAY_MALAYSIA](#MALAY-MALAYSIA) | Dil: Malayca (Malezya) |
| [MALTESE](#MALTESE) | Dil: Maltaca |
| [MANIPURI](#MANIPURI) | Dil: Manipuri |
| [MAORI](#MAORI) | Dil: Maori |
| [MAPUDUNGUN_CHILE](#MAPUDUNGUN-CHILE) | Dil: Mapudungun (Şili) |
| [MARATHI](#MARATHI) | Dil: Marathi |
| [MOHAWK](#MOHAWK) | Dil: Mohawk |
| [MONGOLIAN_CYRILLIC](#MONGOLIAN-CYRILLIC) | Dil: Moğolca (Kiril) |
| [MONGOLIAN_MONGOLIAN](#MONGOLIAN-MONGOLIAN) | Dil: Moğolca (Moğol) |
| [NEPALI](#NEPALI) | Dil: Nepalce |
| [NORTHERN_SAMI_FINLAND](#NORTHERN-SAMI-FINLAND) | Dil: Kuzey Sami (Finlandiya) |
| [NORTHERN_SAMI_NORWAY](#NORTHERN-SAMI-NORWAY) | Dil: Kuzey Sami (Norveç) |
| [NORTHERN_SAMI_SWEDEN](#NORTHERN-SAMI-SWEDEN) | Dil: Kuzey Sami (İsveç) |
| [NORWEGIAN_BOKMAL](#NORWEGIAN-BOKMAL) | Dil: Norveççe Bokmål |
| [NORWEGIAN_NYNORSK](#NORWEGIAN-NYNORSK) | Dil: Norveççe Nynorsk |
| [ORIYA](#ORIYA) | Dil: Oriya |
| [OROMO](#OROMO) | Dil: Oromo |
| [PAPIAMENTU](#PAPIAMENTU) | Dil: Papiamentu |
| [PASHTO](#PASHTO) | Dil: Peştuca |
| [PERSIAN](#PERSIAN) | Dil: Farsça |
| [POLISH](#POLISH) | Dil: Lehçe |
| [PORTUGUESE_BRAZIL](#PORTUGUESE-BRAZIL) | Dil: Portekizce (Brezilya) |
| [PORTUGUESE_PORTUGAL](#PORTUGUESE-PORTUGAL) | Dil: Portekizce (Portekiz) |
| [PUNJABI_INDIA](#PUNJABI-INDIA) | Dil: Pencapça (Hindistan) |
| [PUNJABI_PAKISTAN](#PUNJABI-PAKISTAN) | Dil: Pencapça (Pakistan) |
| [QUECHUA_BOLIVIA](#QUECHUA-BOLIVIA) | Dil: Quechua (Bolivia) |
| [QUECHUA_ECUADOR](#QUECHUA-ECUADOR) | Dil: Quechua (Ecuador) |
| [QUECHUA_PERU](#QUECHUA-PERU) | Dil: Quechua (Peru) |
| [ROMANIAN](#ROMANIAN) | Dil: Rumence |
| [ROMANSH](#ROMANSH) | Dil: Romansh |
| [RUSSIAN](#RUSSIAN) | Dil: Rusça |
| [SAKHA](#SAKHA) | Dil: Saha |
| [SANSKRIT](#SANSKRIT) | Dil: Sanskritçe |
| [SCOTTISH_GAELIC](#SCOTTISH-GAELIC) | Dil: İskoç Galcesi |
| [SERBIAN_CYRILLIC_BOSNIA_AND_HERZEGOVINA](#SERBIAN-CYRILLIC-BOSNIA-AND-HERZEGOVINA) | Dil: Sırpça (Kiril, Bosna Hersek) |
| [SERBIAN_CYRILLIC_SERBIA_AND_MONTENEGRO](#SERBIAN-CYRILLIC-SERBIA-AND-MONTENEGRO) | Dil: Sırpça (Kiril, Sırbistan ve Karadağ) |
| [SERBIAN_LATIN_BOSNIA_AND_HERZEGOVINA](#SERBIAN-LATIN-BOSNIA-AND-HERZEGOVINA) | Dil: Sırpça (Latin, Bosna Hersek) |
| [SERBIAN_LATIN_SERBIA_AND_MONTENEGRO](#SERBIAN-LATIN-SERBIA-AND-MONTENEGRO) | Dil: Sırpça (Latin, Sırbistan ve Karadağ) |
| [SINDHI](#SINDHI) | Dil: Sindhi |
| [SINDHI_DEVANAGARIC](#SINDHI-DEVANAGARIC) | Dil: Sindhi (Devanagari) |
| [SINHALESE](#SINHALESE) | Dil: Sinhala |
| [SLOVAK](#SLOVAK) | Dil: Slovakça |
| [SLOVENIAN](#SLOVENIAN) | Dil: Slovence |
| [SOMALI](#SOMALI) | Dil: Somalice |
| [SORBIAN](#SORBIAN) | Dil: Sorbça |
| [SPANISH_ARGENTINA](#SPANISH-ARGENTINA) | Dil: İspanyolca (Arjantin) |
| [SPANISH_BOLIVIA](#SPANISH-BOLIVIA) | Dil: İspanyolca (Bolivya) |
| [SPANISH_CHILE](#SPANISH-CHILE) | Dil: İspanyolca (Şili) |
| [SPANISH_COLOMBIA](#SPANISH-COLOMBIA) | Dil: İspanyolca (Kolombiya) |
| [SPANISH_COSTA_RICA](#SPANISH-COSTA-RICA) | Dil: İspanyolca (Kosta Rika) |
| [SPANISH_DOMINICAN_REPUBLIC](#SPANISH-DOMINICAN-REPUBLIC) | Dil: İspanyolca (Dominik Cumhuriyeti) |
| [SPANISH_ECUADOR](#SPANISH-ECUADOR) | Dil: İspanyolca (Ekvador) |
| [SPANISH_EL_SALVADOR](#SPANISH-EL-SALVADOR) | Dil: İspanyolca (El Salvador) |
| [SPANISH_GUATEMALA](#SPANISH-GUATEMALA) | Dil: İspanyolca (Guatemala) |
| [SPANISH_HONDURAS](#SPANISH-HONDURAS) | Dil: İspanyolca (Honduras) |
| [SPANISH_MEXICO](#SPANISH-MEXICO) | Dil: İspanyolca (Meksika) |
| [SPANISH_NICARAGUA](#SPANISH-NICARAGUA) | Dil: İspanyolca (Nikaragua) |
| [SPANISH_PANAMA](#SPANISH-PANAMA) | Dil: İspanyolca (Panama) |
| [SPANISH_PARAGUAY](#SPANISH-PARAGUAY) | Dil: İspanyolca (Paraguay) |
| [SPANISH_PERU](#SPANISH-PERU) | Dil: İspanyolca (Peru) |
| [SPANISH_PUERTO_RICO](#SPANISH-PUERTO-RICO) | Dil: İspanyolca (Porto Riko) |
| [SPANISH_SPAIN_MODERN_SORT](#SPANISH-SPAIN-MODERN-SORT) | Dil: İspanyolca (İspanya, Modern Sıralama) |
| [SPANISH_SPAIN_TRADITIONAL_SORT](#SPANISH-SPAIN-TRADITIONAL-SORT) | Dil: İspanyolca (İspanya, Geleneksel Sıralama) |
| [SPANISH_URUGUAY](#SPANISH-URUGUAY) | Dil: İspanyolca (Uruguay) |
| [SPANISH_VENEZUELA](#SPANISH-VENEZUELA) | Dil: İspanyolca (Venezuela) |
| [SUTU](#SUTU) | Dil: Sutu |
| [SWEDISH_FINLAND](#SWEDISH-FINLAND) | Dil: İsveççe (Finlandiya) |
| [SWEDISH_SWEDEN](#SWEDISH-SWEDEN) | Dil: İsveççe (İsveç) |
| [SYRIAC](#SYRIAC) | Dil: Süryanice |
| [TAJIK](#TAJIK) | Dil: Tacikçe |
| [TAMAZIGHT](#TAMAZIGHT) | Dil: Tamazight |
| [TAMAZIGHT_LATIN](#TAMAZIGHT-LATIN) | Dil: Tamazight (Latin) |
| [TAMIL](#TAMIL) | Dil: Tamilce |
| [TATAR](#TATAR) | Dil: Tatarca |
| [TELUGU](#TELUGU) | Dil: Teluguca |
| [THAI](#THAI) | Dil: Thai |
| [TIBETAN_BUTAN](#TIBETAN-BUTAN) | Dil: Tibetan (Bhutan) |
| [TIBETAN_CHINA](#TIBETAN-CHINA) | Dil: Tibetan (China) |
| [TIGRIGNA_ERITREA](#TIGRIGNA-ERITREA) | Dil: Tigrigna (Eritrea) |
| [TIGRIGNA_ETHIOPIA](#TIGRIGNA-ETHIOPIA) | Dil: Tigrigna (Ethiopia) |
| [TSONGA](#TSONGA) | Dil: Tsonga |
| [TSWANA](#TSWANA) | Dil: Tswana |
| [TURKISH](#TURKISH) | Dil: Turkish |
| [TURKMEN](#TURKMEN) | Dil: Turkmen |
| [UKRAINIAN](#UKRAINIAN) | Dil: Ukrainian |
| [URDU](#URDU) | Dil: Urdu |
| [UZBEK_CYRILLIC](#UZBEK-CYRILLIC) | Dil: Uzbek (Cyrillic) |
| [UZBEK_LATIN](#UZBEK-LATIN) | Dil: Uzbek (Latin) |
| [VENDA](#VENDA) | Dil: Venda |
| [VIETNAMESE](#VIETNAMESE) | Dil: Vietnamese |
| [WELSH](#WELSH) | Dil: Welsh |
| [YI](#YI) | Dil: Yi |
| [YIDDISH](#YIDDISH) | Dil: Yiddish |
| [YORUBA](#YORUBA) | Dil: Yoruba |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String editingLanguageName)](#fromName-java.lang.String) |  |
| [getName(int editingLanguage)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int editingLanguage)](#toString-int) |  |
### AFRIKAANS {#AFRIKAANS}
```
public static int AFRIKAANS
```


Dil: Afrikaans

### ALBANIAN {#ALBANIAN}
```
public static int ALBANIAN
```


Dil: Albanian

### ALSATIAN {#ALSATIAN}
```
public static int ALSATIAN
```


Dil: Alsatian

### AMHARIC {#AMHARIC}
```
public static int AMHARIC
```


Dil: Amharic

### ARABIC_ALGERIA {#ARABIC-ALGERIA}
```
public static int ARABIC_ALGERIA
```


Dil: Arabic (Algeria)

### ARABIC_BAHRAIN {#ARABIC-BAHRAIN}
```
public static int ARABIC_BAHRAIN
```


Dil: Arabic (Bahrain)

### ARABIC_EGYPT {#ARABIC-EGYPT}
```
public static int ARABIC_EGYPT
```


Dil: Arabic (Egypt)

### ARABIC_IRAQ {#ARABIC-IRAQ}
```
public static int ARABIC_IRAQ
```


Dil: Arabic (Iraq)

### ARABIC_JORDAN {#ARABIC-JORDAN}
```
public static int ARABIC_JORDAN
```


Dil: Arapça (Ürdün)

### ARABIC_KUWAIT {#ARABIC-KUWAIT}
```
public static int ARABIC_KUWAIT
```


Dil: Arapça (Kuveyt)

### ARABIC_LEBANON {#ARABIC-LEBANON}
```
public static int ARABIC_LEBANON
```


Dil: Arapça (Lübnan)

### ARABIC_LIBYA {#ARABIC-LIBYA}
```
public static int ARABIC_LIBYA
```


Dil: Arapça (Libya)

### ARABIC_MOROCCO {#ARABIC-MOROCCO}
```
public static int ARABIC_MOROCCO
```


Dil: Arapça (Fas)

### ARABIC_OMAN {#ARABIC-OMAN}
```
public static int ARABIC_OMAN
```


Dil: Arapça (Umman)

### ARABIC_QATAR {#ARABIC-QATAR}
```
public static int ARABIC_QATAR
```


Dil: Arapça (Katar)

### ARABIC_SAUDI_ARABIA {#ARABIC-SAUDI-ARABIA}
```
public static int ARABIC_SAUDI_ARABIA
```


Dil: Arapça (Suudi Arabistan)

### ARABIC_SYRIA {#ARABIC-SYRIA}
```
public static int ARABIC_SYRIA
```


Dil: Arapça (Suriye)

### ARABIC_TUNISIA {#ARABIC-TUNISIA}
```
public static int ARABIC_TUNISIA
```


Dil: Arapça (Tunus)

### ARABIC_UAE {#ARABIC-UAE}
```
public static int ARABIC_UAE
```


Dil: Arapça (Birleşik Arap Emirlikleri)

### ARABIC_YEMEN {#ARABIC-YEMEN}
```
public static int ARABIC_YEMEN
```


Dil: Arapça (Yemen)

### ARMENIAN {#ARMENIAN}
```
public static int ARMENIAN
```


Dil: Ermenice

### ASSAMESE {#ASSAMESE}
```
public static int ASSAMESE
```


Dil: Assamca

### AZERBAIJANI_CYRILLIC {#AZERBAIJANI-CYRILLIC}
```
public static int AZERBAIJANI_CYRILLIC
```


Dil: Azerbaycanca (Kiril)

### AZERBAIJANI_LATIN {#AZERBAIJANI-LATIN}
```
public static int AZERBAIJANI_LATIN
```


Dil: Azerbaycanca (Latin)

### BANGLA_BANGLADESH {#BANGLA-BANGLADESH}
```
public static int BANGLA_BANGLADESH
```


Dil: Bangla (Bangladeş)

### BANGLA_INDIA {#BANGLA-INDIA}
```
public static int BANGLA_INDIA
```


Dil: Bangla (Hindistan)

### BASHKIR {#BASHKIR}
```
public static int BASHKIR
```


Dil: Başkurtça

### BASQUE {#BASQUE}
```
public static int BASQUE
```


Dil: Baskça

### BELARUSIAN {#BELARUSIAN}
```
public static int BELARUSIAN
```


Dil: Beyaz Rusça

### BOSNIAN_CYRILLIC {#BOSNIAN-CYRILLIC}
```
public static int BOSNIAN_CYRILLIC
```


Dil: Boşnakça (Kiril)

### BOSNIAN_LATIN {#BOSNIAN-LATIN}
```
public static int BOSNIAN_LATIN
```


Dil: Boşnakça (Latin)

### BRETON {#BRETON}
```
public static int BRETON
```


Dil: Bretonca

### BULGARIAN {#BULGARIAN}
```
public static int BULGARIAN
```


Dil: Bulgarca

### BURMESE {#BURMESE}
```
public static int BURMESE
```


Dil: Burmese

### CATALAN {#CATALAN}
```
public static int CATALAN
```


Dil: Catalan

### CENTRAL_KURDISH_IRAQ {#CENTRAL-KURDISH-IRAQ}
```
public static int CENTRAL_KURDISH_IRAQ
```


Dil: Central Kurdish (Iraq)

### CHEROKEE {#CHEROKEE}
```
public static int CHEROKEE
```


Dil: Cherokee

### CHINESE_HONG_KONG {#CHINESE-HONG-KONG}
```
public static int CHINESE_HONG_KONG
```


Dil: Chinese (Hong Kong)

### CHINESE_MACAO {#CHINESE-MACAO}
```
public static int CHINESE_MACAO
```


Dil: Chinese (Macao)

### CHINESE_PRC {#CHINESE-PRC}
```
public static int CHINESE_PRC
```


Dil: Chinese (PRC)

### CHINESE_SINGAPORE {#CHINESE-SINGAPORE}
```
public static int CHINESE_SINGAPORE
```


Dil: Chinese (Singapore)

### CHINESE_TAIWAN {#CHINESE-TAIWAN}
```
public static int CHINESE_TAIWAN
```


Dil: Chinese (Taiwan)

### CORSICAN {#CORSICAN}
```
public static int CORSICAN
```


Dil: Corsican

### CROATIAN {#CROATIAN}
```
public static int CROATIAN
```


Dil: Croatian

### CROATIAN_BOZNIA_AND_HERZEGOVINA {#CROATIAN-BOZNIA-AND-HERZEGOVINA}
```
public static int CROATIAN_BOZNIA_AND_HERZEGOVINA
```


Dil: Croatian (Bosnia and Herzegovina)

### CZECH {#CZECH}
```
public static int CZECH
```


Dil: Czech

### DANISH {#DANISH}
```
public static int DANISH
```


Dil: Danish

### DIVEHI {#DIVEHI}
```
public static int DIVEHI
```


Dil: Divehi

### DUTCH_BELGIUM {#DUTCH-BELGIUM}
```
public static int DUTCH_BELGIUM
```


Dil: Dutch (Belgium)

### DUTCH_NETHERLANDS {#DUTCH-NETHERLANDS}
```
public static int DUTCH_NETHERLANDS
```


Dil: Dutch (Netherlands)

### EDO {#EDO}
```
public static int EDO
```


Dil: Edo

### ENGLISH_AUSTRALIA {#ENGLISH-AUSTRALIA}
```
public static int ENGLISH_AUSTRALIA
```


Dil: English (Australia)

### ENGLISH_BELIZE {#ENGLISH-BELIZE}
```
public static int ENGLISH_BELIZE
```


Dil: English (Belize)

### ENGLISH_CANADA {#ENGLISH-CANADA}
```
public static int ENGLISH_CANADA
```


Dil: English (Canada)

### ENGLISH_CARIBBEAN {#ENGLISH-CARIBBEAN}
```
public static int ENGLISH_CARIBBEAN
```


Dil: English (Caribbean)

### ENGLISH_HONG_KONG {#ENGLISH-HONG-KONG}
```
public static int ENGLISH_HONG_KONG
```


Dil: English (Hong Kong)

### ENGLISH_INDIA {#ENGLISH-INDIA}
```
public static int ENGLISH_INDIA
```


Dil: English (India)

### ENGLISH_INDONESIA {#ENGLISH-INDONESIA}
```
public static int ENGLISH_INDONESIA
```


Dil: English (Indonesia)

### ENGLISH_IRELAND {#ENGLISH-IRELAND}
```
public static int ENGLISH_IRELAND
```


Dil: İngilizce (İrlanda)

### ENGLISH_JAMAICA {#ENGLISH-JAMAICA}
```
public static int ENGLISH_JAMAICA
```


Dil: İngilizce (Jamaika)

### ENGLISH_MALAYSIA {#ENGLISH-MALAYSIA}
```
public static int ENGLISH_MALAYSIA
```


Dil: İngilizce (Malezya)

### ENGLISH_NEW_ZEALAND {#ENGLISH-NEW-ZEALAND}
```
public static int ENGLISH_NEW_ZEALAND
```


Dil: İngilizce (Yeni Zelanda)

### ENGLISH_PHILIPPINES {#ENGLISH-PHILIPPINES}
```
public static int ENGLISH_PHILIPPINES
```


Dil: İngilizce (Filipinler)

### ENGLISH_SINGAPORE {#ENGLISH-SINGAPORE}
```
public static int ENGLISH_SINGAPORE
```


Dil: İngilizce (Singapur)

### ENGLISH_SOUTH_AFRICA {#ENGLISH-SOUTH-AFRICA}
```
public static int ENGLISH_SOUTH_AFRICA
```


Dil: İngilizce (Güney Afrika)

### ENGLISH_TRINIDAD_AND_TOBAGO {#ENGLISH-TRINIDAD-AND-TOBAGO}
```
public static int ENGLISH_TRINIDAD_AND_TOBAGO
```


Dil: İngilizce (Trinidad ve Tobago)

### ENGLISH_UK {#ENGLISH-UK}
```
public static int ENGLISH_UK
```


Dil: İngilizce (Birleşik Krallık)

### ENGLISH_US {#ENGLISH-US}
```
public static int ENGLISH_US
```


Dil: İngilizce (ABD)

### ENGLISH_ZIMBABWE {#ENGLISH-ZIMBABWE}
```
public static int ENGLISH_ZIMBABWE
```


Dil: İngilizce (Zimbabve)

### ESTONIAN {#ESTONIAN}
```
public static int ESTONIAN
```


Dil: Estonca

### FAEROESE {#FAEROESE}
```
public static int FAEROESE
```


Dil: Faroe Dili

### FILIPINO {#FILIPINO}
```
public static int FILIPINO
```


Dil: Filipince

### FINNISH {#FINNISH}
```
public static int FINNISH
```


Dil: Fince

### FRENCH_BELGIUM {#FRENCH-BELGIUM}
```
public static int FRENCH_BELGIUM
```


Dil: Fransızca (Belçika)

### FRENCH_CANADA {#FRENCH-CANADA}
```
public static int FRENCH_CANADA
```


Dil: Fransızca (Kanada)

### FRENCH_FRANCE {#FRENCH-FRANCE}
```
public static int FRENCH_FRANCE
```


Dil: Fransızca (Fransa)

### FRENCH_LUXEMBOURG {#FRENCH-LUXEMBOURG}
```
public static int FRENCH_LUXEMBOURG
```


Dil: Fransızca (Lüksemburg)

### FRENCH_MONACO {#FRENCH-MONACO}
```
public static int FRENCH_MONACO
```


Dil: Fransızca (Monako)

### FRENCH_SWITZERLAND {#FRENCH-SWITZERLAND}
```
public static int FRENCH_SWITZERLAND
```


Dil: Fransızca (İsviçre)

### FRISIAN {#FRISIAN}
```
public static int FRISIAN
```


Dil: Frizce

### FULAH_LATIN_SENEGAL {#FULAH-LATIN-SENEGAL}
```
public static int FULAH_LATIN_SENEGAL
```


Dil: Fulah (Latin, Senegal)

### FULAH_NIGERIA {#FULAH-NIGERIA}
```
public static int FULAH_NIGERIA
```


Dil: Fulah (Nijerya)

### GALICIAN {#GALICIAN}
```
public static int GALICIAN
```


Dil: Galiçyaca

### GEORGIAN {#GEORGIAN}
```
public static int GEORGIAN
```


Dil: Gürcüce

### GERMAN_AUSTRIA {#GERMAN-AUSTRIA}
```
public static int GERMAN_AUSTRIA
```


Dil: Almanca (Avusturya)

### GERMAN_GERMANY {#GERMAN-GERMANY}
```
public static int GERMAN_GERMANY
```


Dil: Almanca (Almanya)

### GERMAN_LIECHTENSTEIN {#GERMAN-LIECHTENSTEIN}
```
public static int GERMAN_LIECHTENSTEIN
```


Dil: Almanca (Lihtenştayn)

### GERMAN_LUXEMBOURG {#GERMAN-LUXEMBOURG}
```
public static int GERMAN_LUXEMBOURG
```


Dil: Almanca (Lüksemburg)

### GERMAN_SWITZERLAND {#GERMAN-SWITZERLAND}
```
public static int GERMAN_SWITZERLAND
```


Dil: Almanca (İsviçre)

### GREEK {#GREEK}
```
public static int GREEK
```


Dil: Yunanca

### GREENLANDIC {#GREENLANDIC}
```
public static int GREENLANDIC
```


Dil: Grönlandca

### GUARANI {#GUARANI}
```
public static int GUARANI
```


Dil: Guarani

### GUJARATI {#GUJARATI}
```
public static int GUJARATI
```


Dil: Gujaratça

### HAUSA {#HAUSA}
```
public static int HAUSA
```


Dil: Hausa

### HAWAIIAN {#HAWAIIAN}
```
public static int HAWAIIAN
```


Dil: Hawaiice

### HEBREW {#HEBREW}
```
public static int HEBREW
```


Dil: İbranice

### HINDI {#HINDI}
```
public static int HINDI
```


Dil: Hintçe

### HUNGARIAN {#HUNGARIAN}
```
public static int HUNGARIAN
```


Dil: Macarca

### ICELANDIC {#ICELANDIC}
```
public static int ICELANDIC
```


Dil: İzlandca

### IGBO {#IGBO}
```
public static int IGBO
```


Dil: Igbo

### INARI_SAMI_FINLAND {#INARI-SAMI-FINLAND}
```
public static int INARI_SAMI_FINLAND
```


Dil: Inari Samice (Finlandiya)

### INDONESIAN {#INDONESIAN}
```
public static int INDONESIAN
```


Dil: Endonezce

### INUKTITUT_LATIN {#INUKTITUT-LATIN}
```
public static int INUKTITUT_LATIN
```


Dil: İnuktitut (Latin)

### INUKTITUT_SYLLABICS {#INUKTITUT-SYLLABICS}
```
public static int INUKTITUT_SYLLABICS
```


Dil: İnuktitut (Heceleme)

### IRISH {#IRISH}
```
public static int IRISH
```


Dil: İrlandaca

### ISI_XHOSA {#ISI-XHOSA}
```
public static int ISI_XHOSA
```


Dil: IsiXhosa

### ISI_ZULU {#ISI-ZULU}
```
public static int ISI_ZULU
```


Dil: IsiZulu

### ITALIAN_ITALY {#ITALIAN-ITALY}
```
public static int ITALIAN_ITALY
```


Dil: İtalyanca (İtalya)

### ITALIAN_SWITZERLAND {#ITALIAN-SWITZERLAND}
```
public static int ITALIAN_SWITZERLAND
```


Dil: İtalyanca (İsviçre)

### JAPANESE {#JAPANESE}
```
public static int JAPANESE
```


Dil: Japonca

### KANNADA {#KANNADA}
```
public static int KANNADA
```


Dil: Kannada

### KANURI {#KANURI}
```
public static int KANURI
```


Dil: Kanuri

### KASHMIRI {#KASHMIRI}
```
public static int KASHMIRI
```


Dil: Keşmirce

### KASHMIRI_ARABIC {#KASHMIRI-ARABIC}
```
public static int KASHMIRI_ARABIC
```


Dil: Keşmirce (Arapça)

### KAZAKH {#KAZAKH}
```
public static int KAZAKH
```


Dil: Kazakça

### KHMER {#KHMER}
```
public static int KHMER
```


Dil: Khmer

### KICHE {#KICHE}
```
public static int KICHE
```


Dil: Kiche

### KINYARWANDA {#KINYARWANDA}
```
public static int KINYARWANDA
```


Dil: Kinyarwanda

### KISWAHILI {#KISWAHILI}
```
public static int KISWAHILI
```


Dil: Swahili

### KONKANI {#KONKANI}
```
public static int KONKANI
```


Dil: Konkani

### KOREAN {#KOREAN}
```
public static int KOREAN
```


Dil: Korece

### KYRGYZ {#KYRGYZ}
```
public static int KYRGYZ
```


Dil: Kırgızca

### LAO {#LAO}
```
public static int LAO
```


Dil: Lao

### LATIN {#LATIN}
```
public static int LATIN
```


Dil: Latince

### LATVIAN {#LATVIAN}
```
public static int LATVIAN
```


Dil: Letonca

### LITHUANIAN {#LITHUANIAN}
```
public static int LITHUANIAN
```


Dil: Litvanca

### LOWER_SORBIAN {#LOWER-SORBIAN}
```
public static int LOWER_SORBIAN
```


Dil: Aşağı Sorbça

### LULE_SAMI_NORWAY {#LULE-SAMI-NORWAY}
```
public static int LULE_SAMI_NORWAY
```


Dil: Lule Sami (Norveç)

### LULE_SAMI_SWEDEN {#LULE-SAMI-SWEDEN}
```
public static int LULE_SAMI_SWEDEN
```


Dil: Lule Sami (İsveç)

### LUXEMBOUGISH {#LUXEMBOUGISH}
```
public static int LUXEMBOUGISH
```


Dil: Lüksemburgca

### MACEDONIAN {#MACEDONIAN}
```
public static int MACEDONIAN
```


Dil: Makedonca

### MALAYALAM {#MALAYALAM}
```
public static int MALAYALAM
```


Dil: Malayalam

### MALAY_BRUNEI_DARUSSALAM {#MALAY-BRUNEI-DARUSSALAM}
```
public static int MALAY_BRUNEI_DARUSSALAM
```


Dil: Malayca (Brunei Darussalam)

### MALAY_MALAYSIA {#MALAY-MALAYSIA}
```
public static int MALAY_MALAYSIA
```


Dil: Malayca (Malezya)

### MALTESE {#MALTESE}
```
public static int MALTESE
```


Dil: Maltaca

### MANIPURI {#MANIPURI}
```
public static int MANIPURI
```


Dil: Manipuri

### MAORI {#MAORI}
```
public static int MAORI
```


Dil: Maori

### MAPUDUNGUN_CHILE {#MAPUDUNGUN-CHILE}
```
public static int MAPUDUNGUN_CHILE
```


Dil: Mapudungun (Şili)

### MARATHI {#MARATHI}
```
public static int MARATHI
```


Dil: Marathi

### MOHAWK {#MOHAWK}
```
public static int MOHAWK
```


Dil: Mohawk

### MONGOLIAN_CYRILLIC {#MONGOLIAN-CYRILLIC}
```
public static int MONGOLIAN_CYRILLIC
```


Dil: Moğolca (Kiril)

### MONGOLIAN_MONGOLIAN {#MONGOLIAN-MONGOLIAN}
```
public static int MONGOLIAN_MONGOLIAN
```


Dil: Moğolca (Moğol)

### NEPALI {#NEPALI}
```
public static int NEPALI
```


Dil: Nepalce

### NORTHERN_SAMI_FINLAND {#NORTHERN-SAMI-FINLAND}
```
public static int NORTHERN_SAMI_FINLAND
```


Dil: Kuzey Sami (Finlandiya)

### NORTHERN_SAMI_NORWAY {#NORTHERN-SAMI-NORWAY}
```
public static int NORTHERN_SAMI_NORWAY
```


Dil: Kuzey Sami (Norveç)

### NORTHERN_SAMI_SWEDEN {#NORTHERN-SAMI-SWEDEN}
```
public static int NORTHERN_SAMI_SWEDEN
```


Dil: Kuzey Sami (İsveç)

### NORWEGIAN_BOKMAL {#NORWEGIAN-BOKMAL}
```
public static int NORWEGIAN_BOKMAL
```


Dil: Norveççe Bokmål

### NORWEGIAN_NYNORSK {#NORWEGIAN-NYNORSK}
```
public static int NORWEGIAN_NYNORSK
```


Dil: Norveççe Nynorsk

### ORIYA {#ORIYA}
```
public static int ORIYA
```


Dil: Oriya

### OROMO {#OROMO}
```
public static int OROMO
```


Dil: Oromo

### PAPIAMENTU {#PAPIAMENTU}
```
public static int PAPIAMENTU
```


Dil: Papiamentu

### PASHTO {#PASHTO}
```
public static int PASHTO
```


Dil: Peştuca

### PERSIAN {#PERSIAN}
```
public static int PERSIAN
```


Dil: Farsça

### POLISH {#POLISH}
```
public static int POLISH
```


Dil: Lehçe

### PORTUGUESE_BRAZIL {#PORTUGUESE-BRAZIL}
```
public static int PORTUGUESE_BRAZIL
```


Dil: Portekizce (Brezilya)

### PORTUGUESE_PORTUGAL {#PORTUGUESE-PORTUGAL}
```
public static int PORTUGUESE_PORTUGAL
```


Dil: Portekizce (Portekiz)

### PUNJABI_INDIA {#PUNJABI-INDIA}
```
public static int PUNJABI_INDIA
```


Dil: Pencapça (Hindistan)

### PUNJABI_PAKISTAN {#PUNJABI-PAKISTAN}
```
public static int PUNJABI_PAKISTAN
```


Dil: Pencapça (Pakistan)

### QUECHUA_BOLIVIA {#QUECHUA-BOLIVIA}
```
public static int QUECHUA_BOLIVIA
```


Dil: Quechua (Bolivia)

### QUECHUA_ECUADOR {#QUECHUA-ECUADOR}
```
public static int QUECHUA_ECUADOR
```


Dil: Quechua (Ecuador)

### QUECHUA_PERU {#QUECHUA-PERU}
```
public static int QUECHUA_PERU
```


Dil: Quechua (Peru)

### ROMANIAN {#ROMANIAN}
```
public static int ROMANIAN
```


Dil: Rumence

### ROMANSH {#ROMANSH}
```
public static int ROMANSH
```


Dil: Romansh

### RUSSIAN {#RUSSIAN}
```
public static int RUSSIAN
```


Dil: Rusça

### SAKHA {#SAKHA}
```
public static int SAKHA
```


Dil: Saha

### SANSKRIT {#SANSKRIT}
```
public static int SANSKRIT
```


Dil: Sanskritçe

### SCOTTISH_GAELIC {#SCOTTISH-GAELIC}
```
public static int SCOTTISH_GAELIC
```


Dil: İskoç Galcesi

### SERBIAN_CYRILLIC_BOSNIA_AND_HERZEGOVINA {#SERBIAN-CYRILLIC-BOSNIA-AND-HERZEGOVINA}
```
public static int SERBIAN_CYRILLIC_BOSNIA_AND_HERZEGOVINA
```


Dil: Sırpça (Kiril, Bosna Hersek)

### SERBIAN_CYRILLIC_SERBIA_AND_MONTENEGRO {#SERBIAN-CYRILLIC-SERBIA-AND-MONTENEGRO}
```
public static int SERBIAN_CYRILLIC_SERBIA_AND_MONTENEGRO
```


Dil: Sırpça (Kiril, Sırbistan ve Karadağ)

### SERBIAN_LATIN_BOSNIA_AND_HERZEGOVINA {#SERBIAN-LATIN-BOSNIA-AND-HERZEGOVINA}
```
public static int SERBIAN_LATIN_BOSNIA_AND_HERZEGOVINA
```


Dil: Sırpça (Latin, Bosna Hersek)

### SERBIAN_LATIN_SERBIA_AND_MONTENEGRO {#SERBIAN-LATIN-SERBIA-AND-MONTENEGRO}
```
public static int SERBIAN_LATIN_SERBIA_AND_MONTENEGRO
```


Dil: Sırpça (Latin, Sırbistan ve Karadağ)

### SINDHI {#SINDHI}
```
public static int SINDHI
```


Dil: Sindhi

### SINDHI_DEVANAGARIC {#SINDHI-DEVANAGARIC}
```
public static int SINDHI_DEVANAGARIC
```


Dil: Sindhi (Devanagari)

### SINHALESE {#SINHALESE}
```
public static int SINHALESE
```


Dil: Sinhala

### SLOVAK {#SLOVAK}
```
public static int SLOVAK
```


Dil: Slovakça

### SLOVENIAN {#SLOVENIAN}
```
public static int SLOVENIAN
```


Dil: Slovence

### SOMALI {#SOMALI}
```
public static int SOMALI
```


Dil: Somalice

### SORBIAN {#SORBIAN}
```
public static int SORBIAN
```


Dil: Sorbça

### SPANISH_ARGENTINA {#SPANISH-ARGENTINA}
```
public static int SPANISH_ARGENTINA
```


Dil: İspanyolca (Arjantin)

### SPANISH_BOLIVIA {#SPANISH-BOLIVIA}
```
public static int SPANISH_BOLIVIA
```


Dil: İspanyolca (Bolivya)

### SPANISH_CHILE {#SPANISH-CHILE}
```
public static int SPANISH_CHILE
```


Dil: İspanyolca (Şili)

### SPANISH_COLOMBIA {#SPANISH-COLOMBIA}
```
public static int SPANISH_COLOMBIA
```


Dil: İspanyolca (Kolombiya)

### SPANISH_COSTA_RICA {#SPANISH-COSTA-RICA}
```
public static int SPANISH_COSTA_RICA
```


Dil: İspanyolca (Kosta Rika)

### SPANISH_DOMINICAN_REPUBLIC {#SPANISH-DOMINICAN-REPUBLIC}
```
public static int SPANISH_DOMINICAN_REPUBLIC
```


Dil: İspanyolca (Dominik Cumhuriyeti)

### SPANISH_ECUADOR {#SPANISH-ECUADOR}
```
public static int SPANISH_ECUADOR
```


Dil: İspanyolca (Ekvador)

### SPANISH_EL_SALVADOR {#SPANISH-EL-SALVADOR}
```
public static int SPANISH_EL_SALVADOR
```


Dil: İspanyolca (El Salvador)

### SPANISH_GUATEMALA {#SPANISH-GUATEMALA}
```
public static int SPANISH_GUATEMALA
```


Dil: İspanyolca (Guatemala)

### SPANISH_HONDURAS {#SPANISH-HONDURAS}
```
public static int SPANISH_HONDURAS
```


Dil: İspanyolca (Honduras)

### SPANISH_MEXICO {#SPANISH-MEXICO}
```
public static int SPANISH_MEXICO
```


Dil: İspanyolca (Meksika)

### SPANISH_NICARAGUA {#SPANISH-NICARAGUA}
```
public static int SPANISH_NICARAGUA
```


Dil: İspanyolca (Nikaragua)

### SPANISH_PANAMA {#SPANISH-PANAMA}
```
public static int SPANISH_PANAMA
```


Dil: İspanyolca (Panama)

### SPANISH_PARAGUAY {#SPANISH-PARAGUAY}
```
public static int SPANISH_PARAGUAY
```


Dil: İspanyolca (Paraguay)

### SPANISH_PERU {#SPANISH-PERU}
```
public static int SPANISH_PERU
```


Dil: İspanyolca (Peru)

### SPANISH_PUERTO_RICO {#SPANISH-PUERTO-RICO}
```
public static int SPANISH_PUERTO_RICO
```


Dil: İspanyolca (Porto Riko)

### SPANISH_SPAIN_MODERN_SORT {#SPANISH-SPAIN-MODERN-SORT}
```
public static int SPANISH_SPAIN_MODERN_SORT
```


Dil: İspanyolca (İspanya, Modern Sıralama)

### SPANISH_SPAIN_TRADITIONAL_SORT {#SPANISH-SPAIN-TRADITIONAL-SORT}
```
public static int SPANISH_SPAIN_TRADITIONAL_SORT
```


Dil: İspanyolca (İspanya, Geleneksel Sıralama)

### SPANISH_URUGUAY {#SPANISH-URUGUAY}
```
public static int SPANISH_URUGUAY
```


Dil: İspanyolca (Uruguay)

### SPANISH_VENEZUELA {#SPANISH-VENEZUELA}
```
public static int SPANISH_VENEZUELA
```


Dil: İspanyolca (Venezuela)

### SUTU {#SUTU}
```
public static int SUTU
```


Dil: Sutu

### SWEDISH_FINLAND {#SWEDISH-FINLAND}
```
public static int SWEDISH_FINLAND
```


Dil: İsveççe (Finlandiya)

### SWEDISH_SWEDEN {#SWEDISH-SWEDEN}
```
public static int SWEDISH_SWEDEN
```


Dil: İsveççe (İsveç)

### SYRIAC {#SYRIAC}
```
public static int SYRIAC
```


Dil: Süryanice

### TAJIK {#TAJIK}
```
public static int TAJIK
```


Dil: Tacikçe

### TAMAZIGHT {#TAMAZIGHT}
```
public static int TAMAZIGHT
```


Dil: Tamazight

### TAMAZIGHT_LATIN {#TAMAZIGHT-LATIN}
```
public static int TAMAZIGHT_LATIN
```


Dil: Tamazight (Latin)

### TAMIL {#TAMIL}
```
public static int TAMIL
```


Dil: Tamilce

### TATAR {#TATAR}
```
public static int TATAR
```


Dil: Tatarca

### TELUGU {#TELUGU}
```
public static int TELUGU
```


Dil: Teluguca

### THAI {#THAI}
```
public static int THAI
```


Dil: Thai

### TIBETAN_BUTAN {#TIBETAN-BUTAN}
```
public static int TIBETAN_BUTAN
```


Dil: Tibetan (Bhutan)

### TIBETAN_CHINA {#TIBETAN-CHINA}
```
public static int TIBETAN_CHINA
```


Dil: Tibetan (China)

### TIGRIGNA_ERITREA {#TIGRIGNA-ERITREA}
```
public static int TIGRIGNA_ERITREA
```


Dil: Tigrigna (Eritrea)

### TIGRIGNA_ETHIOPIA {#TIGRIGNA-ETHIOPIA}
```
public static int TIGRIGNA_ETHIOPIA
```


Dil: Tigrigna (Ethiopia)

### TSONGA {#TSONGA}
```
public static int TSONGA
```


Dil: Tsonga

### TSWANA {#TSWANA}
```
public static int TSWANA
```


Dil: Tswana

### TURKISH {#TURKISH}
```
public static int TURKISH
```


Dil: Turkish

### TURKMEN {#TURKMEN}
```
public static int TURKMEN
```


Dil: Turkmen

### UKRAINIAN {#UKRAINIAN}
```
public static int UKRAINIAN
```


Dil: Ukrainian

### URDU {#URDU}
```
public static int URDU
```


Dil: Urdu

### UZBEK_CYRILLIC {#UZBEK-CYRILLIC}
```
public static int UZBEK_CYRILLIC
```


Dil: Uzbek (Cyrillic)

### UZBEK_LATIN {#UZBEK-LATIN}
```
public static int UZBEK_LATIN
```


Dil: Uzbek (Latin)

### VENDA {#VENDA}
```
public static int VENDA
```


Dil: Venda

### VIETNAMESE {#VIETNAMESE}
```
public static int VIETNAMESE
```


Dil: Vietnamese

### WELSH {#WELSH}
```
public static int WELSH
```


Dil: Welsh

### YI {#YI}
```
public static int YI
```


Dil: Yi

### YIDDISH {#YIDDISH}
```
public static int YIDDISH
```


Dil: Yiddish

### YORUBA {#YORUBA}
```
public static int YORUBA
```


Dil: Yoruba

### length {#length}
```
public static int length
```


### fromName(String editingLanguageName) {#fromName-java.lang.String}
```
public static int fromName(String editingLanguageName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| editingLanguageName | java.lang.String |  |

**Returns:**
int
### getName(int editingLanguage) {#getName-int}
```
public static String getName(int editingLanguage)
```




**Parameters:**
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| editingLanguage | int |  |

**Returns:**
java.lang.String
