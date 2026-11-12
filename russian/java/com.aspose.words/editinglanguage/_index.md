---
title: "EditingLanguage"
linktitle: "EditingLanguage"
second_title: "Aspose.Words для Java"
description: "Указывает язык редактирования в Java."
type: docs
weight: 182
url: /ru/java/com.aspose.words/editinglanguage/
---

**Inheritance:**
java.lang.Object
```
public class EditingLanguage
```

Указывает язык редактирования.

 **Examples:** 

Показывает, как применить языковые предпочтения при загрузке документа.

```

 LoadOptions loadOptions = new LoadOptions();
 loadOptions.getLanguagePreferences().addEditingLanguage(EditingLanguage.JAPANESE);

 Document doc = new Document(getMyDir() + "No default editing language.docx", loadOptions);

 int localeIdFarEast = doc.getStyles().getDefaultFont().getLocaleIdFarEast();
 System.out.println(localeIdFarEast == EditingLanguage.JAPANESE
         ? "The document either has no any FarEast language set in defaults or it was set to Japanese originally."
         : "The document default FarEast language was set to another than Japanese language originally, so it is not overridden.");
 
```
## Поля

| Поле | Описание |
| --- | --- |
| [AFRIKAANS](#AFRIKAANS) | Язык: Afrikaans |
| [ALBANIAN](#ALBANIAN) | Язык: Albanian |
| [ALSATIAN](#ALSATIAN) | Язык: Alsatian |
| [AMHARIC](#AMHARIC) | Язык: Amharic |
| [ARABIC_ALGERIA](#ARABIC-ALGERIA) | Язык: Arabic (Algeria) |
| [ARABIC_BAHRAIN](#ARABIC-BAHRAIN) | Язык: Arabic (Bahrain) |
| [ARABIC_EGYPT](#ARABIC-EGYPT) | Язык: Arabic (Egypt) |
| [ARABIC_IRAQ](#ARABIC-IRAQ) | Язык: Arabic (Iraq) |
| [ARABIC_JORDAN](#ARABIC-JORDAN) | Язык: арабский (Иордания) |
| [ARABIC_KUWAIT](#ARABIC-KUWAIT) | Язык: арабский (Кувейт) |
| [ARABIC_LEBANON](#ARABIC-LEBANON) | Язык: арабский (Ливан) |
| [ARABIC_LIBYA](#ARABIC-LIBYA) | Язык: арабский (Ливия) |
| [ARABIC_MOROCCO](#ARABIC-MOROCCO) | Язык: арабский (Марокко) |
| [ARABIC_OMAN](#ARABIC-OMAN) | Язык: арабский (Оман) |
| [ARABIC_QATAR](#ARABIC-QATAR) | Язык: арабский (Катар) |
| [ARABIC_SAUDI_ARABIA](#ARABIC-SAUDI-ARABIA) | Язык: арабский (Саудовская Аравия) |
| [ARABIC_SYRIA](#ARABIC-SYRIA) | Язык: арабский (Сирия) |
| [ARABIC_TUNISIA](#ARABIC-TUNISIA) | Язык: арабский (Тунис) |
| [ARABIC_UAE](#ARABIC-UAE) | Язык: арабский (Объединённые Арабские Эмираты) |
| [ARABIC_YEMEN](#ARABIC-YEMEN) | Язык: арабский (Йемен) |
| [ARMENIAN](#ARMENIAN) | Язык: армянский |
| [ASSAMESE](#ASSAMESE) | Язык: ассамский |
| [AZERBAIJANI_CYRILLIC](#AZERBAIJANI-CYRILLIC) | Язык: азербайджанский (кириллица) |
| [AZERBAIJANI_LATIN](#AZERBAIJANI-LATIN) | Язык: азербайджанский (латиница) |
| [BANGLA_BANGLADESH](#BANGLA-BANGLADESH) | Язык: бенгальский (Бангладеш) |
| [BANGLA_INDIA](#BANGLA-INDIA) | Язык: бенгальский (Индия) |
| [BASHKIR](#BASHKIR) | Язык: башкирский |
| [BASQUE](#BASQUE) | Язык: баскский |
| [BELARUSIAN](#BELARUSIAN) | Язык: белорусский |
| [BOSNIAN_CYRILLIC](#BOSNIAN-CYRILLIC) | Язык: боснийский (кириллица) |
| [BOSNIAN_LATIN](#BOSNIAN-LATIN) | Язык: боснийский (латиница) |
| [BRETON](#BRETON) | Язык: бретонский |
| [BULGARIAN](#BULGARIAN) | Язык: болгарский |
| [BURMESE](#BURMESE) | Язык: Бирманский |
| [CATALAN](#CATALAN) | Язык: Каталонский |
| [CENTRAL_KURDISH_IRAQ](#CENTRAL-KURDISH-IRAQ) | Язык: Центральный курдский (Ирак) |
| [CHEROKEE](#CHEROKEE) | Язык: Чероки |
| [CHINESE_HONG_KONG](#CHINESE-HONG-KONG) | Язык: Китайский (Гонконг) |
| [CHINESE_MACAO](#CHINESE-MACAO) | Язык: Китайский (Макао) |
| [CHINESE_PRC](#CHINESE-PRC) | Язык: Китайский (КНР) |
| [CHINESE_SINGAPORE](#CHINESE-SINGAPORE) | Язык: Китайский (Сингапур) |
| [CHINESE_TAIWAN](#CHINESE-TAIWAN) | Язык: Китайский (Тайвань) |
| [CORSICAN](#CORSICAN) | Язык: Корсиканский |
| [CROATIAN](#CROATIAN) | Язык: Хорватский |
| [CROATIAN_BOZNIA_AND_HERZEGOVINA](#CROATIAN-BOZNIA-AND-HERZEGOVINA) | Язык: Хорватский (Босния и Герцеговина) |
| [CZECH](#CZECH) | Язык: Чешский |
| [DANISH](#DANISH) | Язык: Датский |
| [DIVEHI](#DIVEHI) | Язык: Дивехи |
| [DUTCH_BELGIUM](#DUTCH-BELGIUM) | Язык: Нидерландский (Бельгия) |
| [DUTCH_NETHERLANDS](#DUTCH-NETHERLANDS) | Язык: Нидерландский (Нидерланды) |
| [EDO](#EDO) | Язык: Эдо |
| [ENGLISH_AUSTRALIA](#ENGLISH-AUSTRALIA) | Язык: Английский (Австралия) |
| [ENGLISH_BELIZE](#ENGLISH-BELIZE) | Язык: Английский (Белиз) |
| [ENGLISH_CANADA](#ENGLISH-CANADA) | Язык: Английский (Канада) |
| [ENGLISH_CARIBBEAN](#ENGLISH-CARIBBEAN) | Язык: Английский (Карибы) |
| [ENGLISH_HONG_KONG](#ENGLISH-HONG-KONG) | Язык: Английский (Гонконг) |
| [ENGLISH_INDIA](#ENGLISH-INDIA) | Язык: Английский (Индия) |
| [ENGLISH_INDONESIA](#ENGLISH-INDONESIA) | Язык: Английский (Индонезия) |
| [ENGLISH_IRELAND](#ENGLISH-IRELAND) | Язык: английский (Ирландия) |
| [ENGLISH_JAMAICA](#ENGLISH-JAMAICA) | Язык: английский (Ямайка) |
| [ENGLISH_MALAYSIA](#ENGLISH-MALAYSIA) | Язык: английский (Малайзия) |
| [ENGLISH_NEW_ZEALAND](#ENGLISH-NEW-ZEALAND) | Язык: английский (Новая Зеландия) |
| [ENGLISH_PHILIPPINES](#ENGLISH-PHILIPPINES) | Язык: английский (Филиппины) |
| [ENGLISH_SINGAPORE](#ENGLISH-SINGAPORE) | Язык: английский (Сингапур) |
| [ENGLISH_SOUTH_AFRICA](#ENGLISH-SOUTH-AFRICA) | Язык: английский (Южная Африка) |
| [ENGLISH_TRINIDAD_AND_TOBAGO](#ENGLISH-TRINIDAD-AND-TOBAGO) | Язык: английский (Тринидад и Тобаго) |
| [ENGLISH_UK](#ENGLISH-UK) | Язык: английский (Великобритания) |
| [ENGLISH_US](#ENGLISH-US) | Язык: английский (США) |
| [ENGLISH_ZIMBABWE](#ENGLISH-ZIMBABWE) | Язык: английский (Зимбабве) |
| [ESTONIAN](#ESTONIAN) | Язык: эстонский |
| [FAEROESE](#FAEROESE) | Язык: фарерский |
| [FILIPINO](#FILIPINO) | Язык: филиппинский |
| [FINNISH](#FINNISH) | Язык: финский |
| [FRENCH_BELGIUM](#FRENCH-BELGIUM) | Язык: французский (Бельгия) |
| [FRENCH_CANADA](#FRENCH-CANADA) | Язык: французский (Канада) |
| [FRENCH_FRANCE](#FRENCH-FRANCE) | Язык: французский (Франция) |
| [FRENCH_LUXEMBOURG](#FRENCH-LUXEMBOURG) | Язык: французский (Люксембург) |
| [FRENCH_MONACO](#FRENCH-MONACO) | Язык: французский (Монако) |
| [FRENCH_SWITZERLAND](#FRENCH-SWITZERLAND) | Язык: французский (Швейцария) |
| [FRISIAN](#FRISIAN) | Язык: фризский |
| [FULAH_LATIN_SENEGAL](#FULAH-LATIN-SENEGAL) | Язык: фула (латинский, Сенегал) |
| [FULAH_NIGERIA](#FULAH-NIGERIA) | Язык: фула (Нигерия) |
| [GALICIAN](#GALICIAN) | Язык: галисийский |
| [GEORGIAN](#GEORGIAN) | Язык: грузинский |
| [GERMAN_AUSTRIA](#GERMAN-AUSTRIA) | Язык: немецкий (Австрия) |
| [GERMAN_GERMANY](#GERMAN-GERMANY) | Язык: немецкий (Германия) |
| [GERMAN_LIECHTENSTEIN](#GERMAN-LIECHTENSTEIN) | Язык: немецкий (Лихтенштейн) |
| [GERMAN_LUXEMBOURG](#GERMAN-LUXEMBOURG) | Язык: немецкий (Люксембург) |
| [GERMAN_SWITZERLAND](#GERMAN-SWITZERLAND) | Язык: немецкий (Швейцария) |
| [GREEK](#GREEK) | Язык: греческий |
| [GREENLANDIC](#GREENLANDIC) | Язык: гренландский |
| [GUARANI](#GUARANI) | Язык: гуарани |
| [GUJARATI](#GUJARATI) | Язык: гуджарати |
| [HAUSA](#HAUSA) | Язык: хауса |
| [HAWAIIAN](#HAWAIIAN) | Язык: гавайский |
| [HEBREW](#HEBREW) | Язык: иврит |
| [HINDI](#HINDI) | Язык: хинди |
| [HUNGARIAN](#HUNGARIAN) | Язык: венгерский |
| [ICELANDIC](#ICELANDIC) | Язык: исландский |
| [IGBO](#IGBO) | Язык: игбо |
| [INARI_SAMI_FINLAND](#INARI-SAMI-FINLAND) | Язык: инари-саамский (Финляндия) |
| [INDONESIAN](#INDONESIAN) | Язык: индонезийский |
| [INUKTITUT_LATIN](#INUKTITUT-LATIN) | Язык: инуктитут (латиница) |
| [INUKTITUT_SYLLABICS](#INUKTITUT-SYLLABICS) | Язык: инуктитут (силлабика) |
| [IRISH](#IRISH) | Язык: ирландский |
| [ISI_XHOSA](#ISI-XHOSA) | Язык: ксоса |
| [ISI_ZULU](#ISI-ZULU) | Язык: зулу |
| [ITALIAN_ITALY](#ITALIAN-ITALY) | Язык: итальянский (Италия) |
| [ITALIAN_SWITZERLAND](#ITALIAN-SWITZERLAND) | Язык: итальянский (Швейцария) |
| [JAPANESE](#JAPANESE) | Язык: японский |
| [KANNADA](#KANNADA) | Язык: каннада |
| [KANURI](#KANURI) | Язык: канури |
| [KASHMIRI](#KASHMIRI) | Язык: кашмири |
| [KASHMIRI_ARABIC](#KASHMIRI-ARABIC) | Язык: кашмири (арабский) |
| [KAZAKH](#KAZAKH) | Язык: казахский |
| [KHMER](#KHMER) | Язык: кхмерский |
| [KICHE](#KICHE) | Язык: киче |
| [KINYARWANDA](#KINYARWANDA) | Язык: киньяруанда |
| [KISWAHILI](#KISWAHILI) | Язык: суахили |
| [KONKANI](#KONKANI) | Язык: конкани |
| [KOREAN](#KOREAN) | Язык: корейский |
| [KYRGYZ](#KYRGYZ) | Язык: кыргызский |
| [LAO](#LAO) | Язык: лаосский |
| [LATIN](#LATIN) | Язык: латинский |
| [LATVIAN](#LATVIAN) | Язык: латышский |
| [LITHUANIAN](#LITHUANIAN) | Язык: литовский |
| [LOWER_SORBIAN](#LOWER-SORBIAN) | Язык: нижнелужицкий |
| [LULE_SAMI_NORWAY](#LULE-SAMI-NORWAY) | Язык: луле-саамский (Норвегия) |
| [LULE_SAMI_SWEDEN](#LULE-SAMI-SWEDEN) | Язык: луле-саамский (Швеция) |
| [LUXEMBOUGISH](#LUXEMBOUGISH) | Язык: люксембургский |
| [MACEDONIAN](#MACEDONIAN) | Язык: македонский |
| [MALAYALAM](#MALAYALAM) | Язык: малаялам |
| [MALAY_BRUNEI_DARUSSALAM](#MALAY-BRUNEI-DARUSSALAM) | Язык: малайский (Бруней-Даруссалам) |
| [MALAY_MALAYSIA](#MALAY-MALAYSIA) | Язык: малайский (Малайзия) |
| [MALTESE](#MALTESE) | Язык: мальтийский |
| [MANIPURI](#MANIPURI) | Язык: манипури |
| [MAORI](#MAORI) | Язык: маори |
| [MAPUDUNGUN_CHILE](#MAPUDUNGUN-CHILE) | Язык: мапудунгун (Чили) |
| [MARATHI](#MARATHI) | Язык: маратхи |
| [MOHAWK](#MOHAWK) | Язык: мохаук |
| [MONGOLIAN_CYRILLIC](#MONGOLIAN-CYRILLIC) | Язык: монгольский (кириллица) |
| [MONGOLIAN_MONGOLIAN](#MONGOLIAN-MONGOLIAN) | Язык: монгольский (монгольский) |
| [NEPALI](#NEPALI) | Язык: непальский |
| [NORTHERN_SAMI_FINLAND](#NORTHERN-SAMI-FINLAND) | Язык: северносаамский (Финляндия) |
| [NORTHERN_SAMI_NORWAY](#NORTHERN-SAMI-NORWAY) | Язык: северносаамский (Норвегия) |
| [NORTHERN_SAMI_SWEDEN](#NORTHERN-SAMI-SWEDEN) | Язык: северносаамский (Швеция) |
| [NORWEGIAN_BOKMAL](#NORWEGIAN-BOKMAL) | Язык: норвежский букмол |
| [NORWEGIAN_NYNORSK](#NORWEGIAN-NYNORSK) | Язык: норвежский нюнорск |
| [ORIYA](#ORIYA) | Язык: ория |
| [OROMO](#OROMO) | Язык: оромо |
| [PAPIAMENTU](#PAPIAMENTU) | Язык: папиаменто |
| [PASHTO](#PASHTO) | Язык: пушту |
| [PERSIAN](#PERSIAN) | Язык: персидский |
| [POLISH](#POLISH) | Язык: польский |
| [PORTUGUESE_BRAZIL](#PORTUGUESE-BRAZIL) | Язык: португальский (Бразилия) |
| [PORTUGUESE_PORTUGAL](#PORTUGUESE-PORTUGAL) | Язык: португальский (Португалия) |
| [PUNJABI_INDIA](#PUNJABI-INDIA) | Язык: пенджабский (Индия) |
| [PUNJABI_PAKISTAN](#PUNJABI-PAKISTAN) | Язык: пенджабский (Пакистан) |
| [QUECHUA_BOLIVIA](#QUECHUA-BOLIVIA) | Язык: Quechua (Боливия) |
| [QUECHUA_ECUADOR](#QUECHUA-ECUADOR) | Язык: Quechua (Эквадор) |
| [QUECHUA_PERU](#QUECHUA-PERU) | Язык: Quechua (Перу) |
| [ROMANIAN](#ROMANIAN) | Язык: румынский |
| [ROMANSH](#ROMANSH) | Язык: романш |
| [RUSSIAN](#RUSSIAN) | Язык: русский |
| [SAKHA](#SAKHA) | Язык: Саха |
| [SANSKRIT](#SANSKRIT) | Язык: санскрит |
| [SCOTTISH_GAELIC](#SCOTTISH-GAELIC) | Язык: шотландский гэльский |
| [SERBIAN_CYRILLIC_BOSNIA_AND_HERZEGOVINA](#SERBIAN-CYRILLIC-BOSNIA-AND-HERZEGOVINA) | Язык: сербский (кириллица, Босния и Герцеговина) |
| [SERBIAN_CYRILLIC_SERBIA_AND_MONTENEGRO](#SERBIAN-CYRILLIC-SERBIA-AND-MONTENEGRO) | Язык: сербский (кириллица, Сербия и Черногория) |
| [SERBIAN_LATIN_BOSNIA_AND_HERZEGOVINA](#SERBIAN-LATIN-BOSNIA-AND-HERZEGOVINA) | Язык: сербский (латинский, Босния и Герцеговина) |
| [SERBIAN_LATIN_SERBIA_AND_MONTENEGRO](#SERBIAN-LATIN-SERBIA-AND-MONTENEGRO) | Язык: сербский (латинский, Сербия и Черногория) |
| [SINDHI](#SINDHI) | Язык: синдхи |
| [SINDHI_DEVANAGARIC](#SINDHI-DEVANAGARIC) | Язык: синдхи (Деванагари) |
| [SINHALESE](#SINHALESE) | Язык: сингальский |
| [SLOVAK](#SLOVAK) | Язык: словацкий |
| [SLOVENIAN](#SLOVENIAN) | Язык: словенский |
| [SOMALI](#SOMALI) | Язык: сомалийский |
| [SORBIAN](#SORBIAN) | Язык: сорбский |
| [SPANISH_ARGENTINA](#SPANISH-ARGENTINA) | Язык: испанский (Аргентина) |
| [SPANISH_BOLIVIA](#SPANISH-BOLIVIA) | Язык: испанский (Боливия) |
| [SPANISH_CHILE](#SPANISH-CHILE) | Язык: испанский (Чили) |
| [SPANISH_COLOMBIA](#SPANISH-COLOMBIA) | Язык: испанский (Колумбия) |
| [SPANISH_COSTA_RICA](#SPANISH-COSTA-RICA) | Язык: испанский (Коста-Рика) |
| [SPANISH_DOMINICAN_REPUBLIC](#SPANISH-DOMINICAN-REPUBLIC) | Язык: Испанский (Доминиканская Республика) |
| [SPANISH_ECUADOR](#SPANISH-ECUADOR) | Язык: Испанский (Эквадор) |
| [SPANISH_EL_SALVADOR](#SPANISH-EL-SALVADOR) | Язык: Испанский (Эль-Сальвадор) |
| [SPANISH_GUATEMALA](#SPANISH-GUATEMALA) | Язык: Испанский (Гватемала) |
| [SPANISH_HONDURAS](#SPANISH-HONDURAS) | Язык: Испанский (Гондурас) |
| [SPANISH_MEXICO](#SPANISH-MEXICO) | Язык: Испанский (Мексика) |
| [SPANISH_NICARAGUA](#SPANISH-NICARAGUA) | Язык: Испанский (Никарагуа) |
| [SPANISH_PANAMA](#SPANISH-PANAMA) | Язык: Испанский (Панама) |
| [SPANISH_PARAGUAY](#SPANISH-PARAGUAY) | Язык: Испанский (Парагвай) |
| [SPANISH_PERU](#SPANISH-PERU) | Язык: Испанский (Перу) |
| [SPANISH_PUERTO_RICO](#SPANISH-PUERTO-RICO) | Язык: Испанский (Пуэрто-Рико) |
| [SPANISH_SPAIN_MODERN_SORT](#SPANISH-SPAIN-MODERN-SORT) | Язык: Испанский (Испания, современный порядок) |
| [SPANISH_SPAIN_TRADITIONAL_SORT](#SPANISH-SPAIN-TRADITIONAL-SORT) | Язык: Испанский (Испания, традиционный порядок) |
| [SPANISH_URUGUAY](#SPANISH-URUGUAY) | Язык: Испанский (Уругвай) |
| [SPANISH_VENEZUELA](#SPANISH-VENEZUELA) | Язык: Испанский (Венесуэла) |
| [SUTU](#SUTU) | Язык: Суту |
| [SWEDISH_FINLAND](#SWEDISH-FINLAND) | Язык: Шведский (Финляндия) |
| [SWEDISH_SWEDEN](#SWEDISH-SWEDEN) | Язык: Шведский (Швеция) |
| [SYRIAC](#SYRIAC) | Язык: Сирийский |
| [TAJIK](#TAJIK) | Язык: Таджикский |
| [TAMAZIGHT](#TAMAZIGHT) | Язык: Тамазигхт |
| [TAMAZIGHT_LATIN](#TAMAZIGHT-LATIN) | Язык: Тамазигхт (Латинский) |
| [TAMIL](#TAMIL) | Язык: Тамильский |
| [TATAR](#TATAR) | Язык: Татарский |
| [TELUGU](#TELUGU) | Язык: Телугу |
| [THAI](#THAI) | Язык: Thai |
| [TIBETAN_BUTAN](#TIBETAN-BUTAN) | Язык: Tibetan (Bhutan) |
| [TIBETAN_CHINA](#TIBETAN-CHINA) | Язык: Tibetan (China) |
| [TIGRIGNA_ERITREA](#TIGRIGNA-ERITREA) | Язык: Tigrigna (Eritrea) |
| [TIGRIGNA_ETHIOPIA](#TIGRIGNA-ETHIOPIA) | Язык: Tigrigna (Ethiopia) |
| [TSONGA](#TSONGA) | Язык: Tsonga |
| [TSWANA](#TSWANA) | Язык: Tswana |
| [TURKISH](#TURKISH) | Язык: Turkish |
| [TURKMEN](#TURKMEN) | Язык: Turkmen |
| [UKRAINIAN](#UKRAINIAN) | Язык: Ukrainian |
| [URDU](#URDU) | Язык: Urdu |
| [UZBEK_CYRILLIC](#UZBEK-CYRILLIC) | Язык: Uzbek (Cyrillic) |
| [UZBEK_LATIN](#UZBEK-LATIN) | Язык: Uzbek (Latin) |
| [VENDA](#VENDA) | Язык: Venda |
| [VIETNAMESE](#VIETNAMESE) | Язык: Vietnamese |
| [WELSH](#WELSH) | Язык: Welsh |
| [YI](#YI) | Язык: Yi |
| [YIDDISH](#YIDDISH) | Язык: Yiddish |
| [YORUBA](#YORUBA) | Язык: Yoruba |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String editingLanguageName)](#fromName-java.lang.String) |  |
| [getName(int editingLanguage)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int editingLanguage)](#toString-int) |  |
### AFRIKAANS {#AFRIKAANS}
```
public static int AFRIKAANS
```


Язык: Afrikaans

### ALBANIAN {#ALBANIAN}
```
public static int ALBANIAN
```


Язык: Albanian

### ALSATIAN {#ALSATIAN}
```
public static int ALSATIAN
```


Язык: Alsatian

### AMHARIC {#AMHARIC}
```
public static int AMHARIC
```


Язык: Amharic

### ARABIC_ALGERIA {#ARABIC-ALGERIA}
```
public static int ARABIC_ALGERIA
```


Язык: Arabic (Algeria)

### ARABIC_BAHRAIN {#ARABIC-BAHRAIN}
```
public static int ARABIC_BAHRAIN
```


Язык: Arabic (Bahrain)

### ARABIC_EGYPT {#ARABIC-EGYPT}
```
public static int ARABIC_EGYPT
```


Язык: Arabic (Egypt)

### ARABIC_IRAQ {#ARABIC-IRAQ}
```
public static int ARABIC_IRAQ
```


Язык: Arabic (Iraq)

### ARABIC_JORDAN {#ARABIC-JORDAN}
```
public static int ARABIC_JORDAN
```


Язык: арабский (Иордания)

### ARABIC_KUWAIT {#ARABIC-KUWAIT}
```
public static int ARABIC_KUWAIT
```


Язык: арабский (Кувейт)

### ARABIC_LEBANON {#ARABIC-LEBANON}
```
public static int ARABIC_LEBANON
```


Язык: арабский (Ливан)

### ARABIC_LIBYA {#ARABIC-LIBYA}
```
public static int ARABIC_LIBYA
```


Язык: арабский (Ливия)

### ARABIC_MOROCCO {#ARABIC-MOROCCO}
```
public static int ARABIC_MOROCCO
```


Язык: арабский (Марокко)

### ARABIC_OMAN {#ARABIC-OMAN}
```
public static int ARABIC_OMAN
```


Язык: арабский (Оман)

### ARABIC_QATAR {#ARABIC-QATAR}
```
public static int ARABIC_QATAR
```


Язык: арабский (Катар)

### ARABIC_SAUDI_ARABIA {#ARABIC-SAUDI-ARABIA}
```
public static int ARABIC_SAUDI_ARABIA
```


Язык: арабский (Саудовская Аравия)

### ARABIC_SYRIA {#ARABIC-SYRIA}
```
public static int ARABIC_SYRIA
```


Язык: арабский (Сирия)

### ARABIC_TUNISIA {#ARABIC-TUNISIA}
```
public static int ARABIC_TUNISIA
```


Язык: арабский (Тунис)

### ARABIC_UAE {#ARABIC-UAE}
```
public static int ARABIC_UAE
```


Язык: арабский (Объединённые Арабские Эмираты)

### ARABIC_YEMEN {#ARABIC-YEMEN}
```
public static int ARABIC_YEMEN
```


Язык: арабский (Йемен)

### ARMENIAN {#ARMENIAN}
```
public static int ARMENIAN
```


Язык: армянский

### ASSAMESE {#ASSAMESE}
```
public static int ASSAMESE
```


Язык: ассамский

### AZERBAIJANI_CYRILLIC {#AZERBAIJANI-CYRILLIC}
```
public static int AZERBAIJANI_CYRILLIC
```


Язык: азербайджанский (кириллица)

### AZERBAIJANI_LATIN {#AZERBAIJANI-LATIN}
```
public static int AZERBAIJANI_LATIN
```


Язык: азербайджанский (латиница)

### BANGLA_BANGLADESH {#BANGLA-BANGLADESH}
```
public static int BANGLA_BANGLADESH
```


Язык: бенгальский (Бангладеш)

### BANGLA_INDIA {#BANGLA-INDIA}
```
public static int BANGLA_INDIA
```


Язык: бенгальский (Индия)

### BASHKIR {#BASHKIR}
```
public static int BASHKIR
```


Язык: башкирский

### BASQUE {#BASQUE}
```
public static int BASQUE
```


Язык: баскский

### BELARUSIAN {#BELARUSIAN}
```
public static int BELARUSIAN
```


Язык: белорусский

### BOSNIAN_CYRILLIC {#BOSNIAN-CYRILLIC}
```
public static int BOSNIAN_CYRILLIC
```


Язык: боснийский (кириллица)

### BOSNIAN_LATIN {#BOSNIAN-LATIN}
```
public static int BOSNIAN_LATIN
```


Язык: боснийский (латиница)

### BRETON {#BRETON}
```
public static int BRETON
```


Язык: бретонский

### BULGARIAN {#BULGARIAN}
```
public static int BULGARIAN
```


Язык: болгарский

### BURMESE {#BURMESE}
```
public static int BURMESE
```


Язык: Бирманский

### CATALAN {#CATALAN}
```
public static int CATALAN
```


Язык: Каталонский

### CENTRAL_KURDISH_IRAQ {#CENTRAL-KURDISH-IRAQ}
```
public static int CENTRAL_KURDISH_IRAQ
```


Язык: Центральный курдский (Ирак)

### CHEROKEE {#CHEROKEE}
```
public static int CHEROKEE
```


Язык: Чероки

### CHINESE_HONG_KONG {#CHINESE-HONG-KONG}
```
public static int CHINESE_HONG_KONG
```


Язык: Китайский (Гонконг)

### CHINESE_MACAO {#CHINESE-MACAO}
```
public static int CHINESE_MACAO
```


Язык: Китайский (Макао)

### CHINESE_PRC {#CHINESE-PRC}
```
public static int CHINESE_PRC
```


Язык: Китайский (КНР)

### CHINESE_SINGAPORE {#CHINESE-SINGAPORE}
```
public static int CHINESE_SINGAPORE
```


Язык: Китайский (Сингапур)

### CHINESE_TAIWAN {#CHINESE-TAIWAN}
```
public static int CHINESE_TAIWAN
```


Язык: Китайский (Тайвань)

### CORSICAN {#CORSICAN}
```
public static int CORSICAN
```


Язык: Корсиканский

### CROATIAN {#CROATIAN}
```
public static int CROATIAN
```


Язык: Хорватский

### CROATIAN_BOZNIA_AND_HERZEGOVINA {#CROATIAN-BOZNIA-AND-HERZEGOVINA}
```
public static int CROATIAN_BOZNIA_AND_HERZEGOVINA
```


Язык: Хорватский (Босния и Герцеговина)

### CZECH {#CZECH}
```
public static int CZECH
```


Язык: Чешский

### DANISH {#DANISH}
```
public static int DANISH
```


Язык: Датский

### DIVEHI {#DIVEHI}
```
public static int DIVEHI
```


Язык: Дивехи

### DUTCH_BELGIUM {#DUTCH-BELGIUM}
```
public static int DUTCH_BELGIUM
```


Язык: Нидерландский (Бельгия)

### DUTCH_NETHERLANDS {#DUTCH-NETHERLANDS}
```
public static int DUTCH_NETHERLANDS
```


Язык: Нидерландский (Нидерланды)

### EDO {#EDO}
```
public static int EDO
```


Язык: Эдо

### ENGLISH_AUSTRALIA {#ENGLISH-AUSTRALIA}
```
public static int ENGLISH_AUSTRALIA
```


Язык: Английский (Австралия)

### ENGLISH_BELIZE {#ENGLISH-BELIZE}
```
public static int ENGLISH_BELIZE
```


Язык: Английский (Белиз)

### ENGLISH_CANADA {#ENGLISH-CANADA}
```
public static int ENGLISH_CANADA
```


Язык: Английский (Канада)

### ENGLISH_CARIBBEAN {#ENGLISH-CARIBBEAN}
```
public static int ENGLISH_CARIBBEAN
```


Язык: Английский (Карибы)

### ENGLISH_HONG_KONG {#ENGLISH-HONG-KONG}
```
public static int ENGLISH_HONG_KONG
```


Язык: Английский (Гонконг)

### ENGLISH_INDIA {#ENGLISH-INDIA}
```
public static int ENGLISH_INDIA
```


Язык: Английский (Индия)

### ENGLISH_INDONESIA {#ENGLISH-INDONESIA}
```
public static int ENGLISH_INDONESIA
```


Язык: Английский (Индонезия)

### ENGLISH_IRELAND {#ENGLISH-IRELAND}
```
public static int ENGLISH_IRELAND
```


Язык: английский (Ирландия)

### ENGLISH_JAMAICA {#ENGLISH-JAMAICA}
```
public static int ENGLISH_JAMAICA
```


Язык: английский (Ямайка)

### ENGLISH_MALAYSIA {#ENGLISH-MALAYSIA}
```
public static int ENGLISH_MALAYSIA
```


Язык: английский (Малайзия)

### ENGLISH_NEW_ZEALAND {#ENGLISH-NEW-ZEALAND}
```
public static int ENGLISH_NEW_ZEALAND
```


Язык: английский (Новая Зеландия)

### ENGLISH_PHILIPPINES {#ENGLISH-PHILIPPINES}
```
public static int ENGLISH_PHILIPPINES
```


Язык: английский (Филиппины)

### ENGLISH_SINGAPORE {#ENGLISH-SINGAPORE}
```
public static int ENGLISH_SINGAPORE
```


Язык: английский (Сингапур)

### ENGLISH_SOUTH_AFRICA {#ENGLISH-SOUTH-AFRICA}
```
public static int ENGLISH_SOUTH_AFRICA
```


Язык: английский (Южная Африка)

### ENGLISH_TRINIDAD_AND_TOBAGO {#ENGLISH-TRINIDAD-AND-TOBAGO}
```
public static int ENGLISH_TRINIDAD_AND_TOBAGO
```


Язык: английский (Тринидад и Тобаго)

### ENGLISH_UK {#ENGLISH-UK}
```
public static int ENGLISH_UK
```


Язык: английский (Великобритания)

### ENGLISH_US {#ENGLISH-US}
```
public static int ENGLISH_US
```


Язык: английский (США)

### ENGLISH_ZIMBABWE {#ENGLISH-ZIMBABWE}
```
public static int ENGLISH_ZIMBABWE
```


Язык: английский (Зимбабве)

### ESTONIAN {#ESTONIAN}
```
public static int ESTONIAN
```


Язык: эстонский

### FAEROESE {#FAEROESE}
```
public static int FAEROESE
```


Язык: фарерский

### FILIPINO {#FILIPINO}
```
public static int FILIPINO
```


Язык: филиппинский

### FINNISH {#FINNISH}
```
public static int FINNISH
```


Язык: финский

### FRENCH_BELGIUM {#FRENCH-BELGIUM}
```
public static int FRENCH_BELGIUM
```


Язык: французский (Бельгия)

### FRENCH_CANADA {#FRENCH-CANADA}
```
public static int FRENCH_CANADA
```


Язык: французский (Канада)

### FRENCH_FRANCE {#FRENCH-FRANCE}
```
public static int FRENCH_FRANCE
```


Язык: французский (Франция)

### FRENCH_LUXEMBOURG {#FRENCH-LUXEMBOURG}
```
public static int FRENCH_LUXEMBOURG
```


Язык: французский (Люксембург)

### FRENCH_MONACO {#FRENCH-MONACO}
```
public static int FRENCH_MONACO
```


Язык: французский (Монако)

### FRENCH_SWITZERLAND {#FRENCH-SWITZERLAND}
```
public static int FRENCH_SWITZERLAND
```


Язык: французский (Швейцария)

### FRISIAN {#FRISIAN}
```
public static int FRISIAN
```


Язык: фризский

### FULAH_LATIN_SENEGAL {#FULAH-LATIN-SENEGAL}
```
public static int FULAH_LATIN_SENEGAL
```


Язык: фула (латинский, Сенегал)

### FULAH_NIGERIA {#FULAH-NIGERIA}
```
public static int FULAH_NIGERIA
```


Язык: фула (Нигерия)

### GALICIAN {#GALICIAN}
```
public static int GALICIAN
```


Язык: галисийский

### GEORGIAN {#GEORGIAN}
```
public static int GEORGIAN
```


Язык: грузинский

### GERMAN_AUSTRIA {#GERMAN-AUSTRIA}
```
public static int GERMAN_AUSTRIA
```


Язык: немецкий (Австрия)

### GERMAN_GERMANY {#GERMAN-GERMANY}
```
public static int GERMAN_GERMANY
```


Язык: немецкий (Германия)

### GERMAN_LIECHTENSTEIN {#GERMAN-LIECHTENSTEIN}
```
public static int GERMAN_LIECHTENSTEIN
```


Язык: немецкий (Лихтенштейн)

### GERMAN_LUXEMBOURG {#GERMAN-LUXEMBOURG}
```
public static int GERMAN_LUXEMBOURG
```


Язык: немецкий (Люксембург)

### GERMAN_SWITZERLAND {#GERMAN-SWITZERLAND}
```
public static int GERMAN_SWITZERLAND
```


Язык: немецкий (Швейцария)

### GREEK {#GREEK}
```
public static int GREEK
```


Язык: греческий

### GREENLANDIC {#GREENLANDIC}
```
public static int GREENLANDIC
```


Язык: гренландский

### GUARANI {#GUARANI}
```
public static int GUARANI
```


Язык: гуарани

### GUJARATI {#GUJARATI}
```
public static int GUJARATI
```


Язык: гуджарати

### HAUSA {#HAUSA}
```
public static int HAUSA
```


Язык: хауса

### HAWAIIAN {#HAWAIIAN}
```
public static int HAWAIIAN
```


Язык: гавайский

### HEBREW {#HEBREW}
```
public static int HEBREW
```


Язык: иврит

### HINDI {#HINDI}
```
public static int HINDI
```


Язык: хинди

### HUNGARIAN {#HUNGARIAN}
```
public static int HUNGARIAN
```


Язык: венгерский

### ICELANDIC {#ICELANDIC}
```
public static int ICELANDIC
```


Язык: исландский

### IGBO {#IGBO}
```
public static int IGBO
```


Язык: игбо

### INARI_SAMI_FINLAND {#INARI-SAMI-FINLAND}
```
public static int INARI_SAMI_FINLAND
```


Язык: инари-саамский (Финляндия)

### INDONESIAN {#INDONESIAN}
```
public static int INDONESIAN
```


Язык: индонезийский

### INUKTITUT_LATIN {#INUKTITUT-LATIN}
```
public static int INUKTITUT_LATIN
```


Язык: инуктитут (латиница)

### INUKTITUT_SYLLABICS {#INUKTITUT-SYLLABICS}
```
public static int INUKTITUT_SYLLABICS
```


Язык: инуктитут (силлабика)

### IRISH {#IRISH}
```
public static int IRISH
```


Язык: ирландский

### ISI_XHOSA {#ISI-XHOSA}
```
public static int ISI_XHOSA
```


Язык: ксоса

### ISI_ZULU {#ISI-ZULU}
```
public static int ISI_ZULU
```


Язык: зулу

### ITALIAN_ITALY {#ITALIAN-ITALY}
```
public static int ITALIAN_ITALY
```


Язык: итальянский (Италия)

### ITALIAN_SWITZERLAND {#ITALIAN-SWITZERLAND}
```
public static int ITALIAN_SWITZERLAND
```


Язык: итальянский (Швейцария)

### JAPANESE {#JAPANESE}
```
public static int JAPANESE
```


Язык: японский

### KANNADA {#KANNADA}
```
public static int KANNADA
```


Язык: каннада

### KANURI {#KANURI}
```
public static int KANURI
```


Язык: канури

### KASHMIRI {#KASHMIRI}
```
public static int KASHMIRI
```


Язык: кашмири

### KASHMIRI_ARABIC {#KASHMIRI-ARABIC}
```
public static int KASHMIRI_ARABIC
```


Язык: кашмири (арабский)

### KAZAKH {#KAZAKH}
```
public static int KAZAKH
```


Язык: казахский

### KHMER {#KHMER}
```
public static int KHMER
```


Язык: кхмерский

### KICHE {#KICHE}
```
public static int KICHE
```


Язык: киче

### KINYARWANDA {#KINYARWANDA}
```
public static int KINYARWANDA
```


Язык: киньяруанда

### KISWAHILI {#KISWAHILI}
```
public static int KISWAHILI
```


Язык: суахили

### KONKANI {#KONKANI}
```
public static int KONKANI
```


Язык: конкани

### KOREAN {#KOREAN}
```
public static int KOREAN
```


Язык: корейский

### KYRGYZ {#KYRGYZ}
```
public static int KYRGYZ
```


Язык: кыргызский

### LAO {#LAO}
```
public static int LAO
```


Язык: лаосский

### LATIN {#LATIN}
```
public static int LATIN
```


Язык: латинский

### LATVIAN {#LATVIAN}
```
public static int LATVIAN
```


Язык: латышский

### LITHUANIAN {#LITHUANIAN}
```
public static int LITHUANIAN
```


Язык: литовский

### LOWER_SORBIAN {#LOWER-SORBIAN}
```
public static int LOWER_SORBIAN
```


Язык: нижнелужицкий

### LULE_SAMI_NORWAY {#LULE-SAMI-NORWAY}
```
public static int LULE_SAMI_NORWAY
```


Язык: луле-саамский (Норвегия)

### LULE_SAMI_SWEDEN {#LULE-SAMI-SWEDEN}
```
public static int LULE_SAMI_SWEDEN
```


Язык: луле-саамский (Швеция)

### LUXEMBOUGISH {#LUXEMBOUGISH}
```
public static int LUXEMBOUGISH
```


Язык: люксембургский

### MACEDONIAN {#MACEDONIAN}
```
public static int MACEDONIAN
```


Язык: македонский

### MALAYALAM {#MALAYALAM}
```
public static int MALAYALAM
```


Язык: малаялам

### MALAY_BRUNEI_DARUSSALAM {#MALAY-BRUNEI-DARUSSALAM}
```
public static int MALAY_BRUNEI_DARUSSALAM
```


Язык: малайский (Бруней-Даруссалам)

### MALAY_MALAYSIA {#MALAY-MALAYSIA}
```
public static int MALAY_MALAYSIA
```


Язык: малайский (Малайзия)

### MALTESE {#MALTESE}
```
public static int MALTESE
```


Язык: мальтийский

### MANIPURI {#MANIPURI}
```
public static int MANIPURI
```


Язык: манипури

### MAORI {#MAORI}
```
public static int MAORI
```


Язык: маори

### MAPUDUNGUN_CHILE {#MAPUDUNGUN-CHILE}
```
public static int MAPUDUNGUN_CHILE
```


Язык: мапудунгун (Чили)

### MARATHI {#MARATHI}
```
public static int MARATHI
```


Язык: маратхи

### MOHAWK {#MOHAWK}
```
public static int MOHAWK
```


Язык: мохаук

### MONGOLIAN_CYRILLIC {#MONGOLIAN-CYRILLIC}
```
public static int MONGOLIAN_CYRILLIC
```


Язык: монгольский (кириллица)

### MONGOLIAN_MONGOLIAN {#MONGOLIAN-MONGOLIAN}
```
public static int MONGOLIAN_MONGOLIAN
```


Язык: монгольский (монгольский)

### NEPALI {#NEPALI}
```
public static int NEPALI
```


Язык: непальский

### NORTHERN_SAMI_FINLAND {#NORTHERN-SAMI-FINLAND}
```
public static int NORTHERN_SAMI_FINLAND
```


Язык: северносаамский (Финляндия)

### NORTHERN_SAMI_NORWAY {#NORTHERN-SAMI-NORWAY}
```
public static int NORTHERN_SAMI_NORWAY
```


Язык: северносаамский (Норвегия)

### NORTHERN_SAMI_SWEDEN {#NORTHERN-SAMI-SWEDEN}
```
public static int NORTHERN_SAMI_SWEDEN
```


Язык: северносаамский (Швеция)

### NORWEGIAN_BOKMAL {#NORWEGIAN-BOKMAL}
```
public static int NORWEGIAN_BOKMAL
```


Язык: норвежский букмол

### NORWEGIAN_NYNORSK {#NORWEGIAN-NYNORSK}
```
public static int NORWEGIAN_NYNORSK
```


Язык: норвежский нюнорск

### ORIYA {#ORIYA}
```
public static int ORIYA
```


Язык: ория

### OROMO {#OROMO}
```
public static int OROMO
```


Язык: оромо

### PAPIAMENTU {#PAPIAMENTU}
```
public static int PAPIAMENTU
```


Язык: папиаменто

### PASHTO {#PASHTO}
```
public static int PASHTO
```


Язык: пушту

### PERSIAN {#PERSIAN}
```
public static int PERSIAN
```


Язык: персидский

### POLISH {#POLISH}
```
public static int POLISH
```


Язык: польский

### PORTUGUESE_BRAZIL {#PORTUGUESE-BRAZIL}
```
public static int PORTUGUESE_BRAZIL
```


Язык: португальский (Бразилия)

### PORTUGUESE_PORTUGAL {#PORTUGUESE-PORTUGAL}
```
public static int PORTUGUESE_PORTUGAL
```


Язык: португальский (Португалия)

### PUNJABI_INDIA {#PUNJABI-INDIA}
```
public static int PUNJABI_INDIA
```


Язык: пенджабский (Индия)

### PUNJABI_PAKISTAN {#PUNJABI-PAKISTAN}
```
public static int PUNJABI_PAKISTAN
```


Язык: пенджабский (Пакистан)

### QUECHUA_BOLIVIA {#QUECHUA-BOLIVIA}
```
public static int QUECHUA_BOLIVIA
```


Язык: Quechua (Боливия)

### QUECHUA_ECUADOR {#QUECHUA-ECUADOR}
```
public static int QUECHUA_ECUADOR
```


Язык: Quechua (Эквадор)

### QUECHUA_PERU {#QUECHUA-PERU}
```
public static int QUECHUA_PERU
```


Язык: Quechua (Перу)

### ROMANIAN {#ROMANIAN}
```
public static int ROMANIAN
```


Язык: румынский

### ROMANSH {#ROMANSH}
```
public static int ROMANSH
```


Язык: романш

### RUSSIAN {#RUSSIAN}
```
public static int RUSSIAN
```


Язык: русский

### SAKHA {#SAKHA}
```
public static int SAKHA
```


Язык: Саха

### SANSKRIT {#SANSKRIT}
```
public static int SANSKRIT
```


Язык: санскрит

### SCOTTISH_GAELIC {#SCOTTISH-GAELIC}
```
public static int SCOTTISH_GAELIC
```


Язык: шотландский гэльский

### SERBIAN_CYRILLIC_BOSNIA_AND_HERZEGOVINA {#SERBIAN-CYRILLIC-BOSNIA-AND-HERZEGOVINA}
```
public static int SERBIAN_CYRILLIC_BOSNIA_AND_HERZEGOVINA
```


Язык: сербский (кириллица, Босния и Герцеговина)

### SERBIAN_CYRILLIC_SERBIA_AND_MONTENEGRO {#SERBIAN-CYRILLIC-SERBIA-AND-MONTENEGRO}
```
public static int SERBIAN_CYRILLIC_SERBIA_AND_MONTENEGRO
```


Язык: сербский (кириллица, Сербия и Черногория)

### SERBIAN_LATIN_BOSNIA_AND_HERZEGOVINA {#SERBIAN-LATIN-BOSNIA-AND-HERZEGOVINA}
```
public static int SERBIAN_LATIN_BOSNIA_AND_HERZEGOVINA
```


Язык: сербский (латинский, Босния и Герцеговина)

### SERBIAN_LATIN_SERBIA_AND_MONTENEGRO {#SERBIAN-LATIN-SERBIA-AND-MONTENEGRO}
```
public static int SERBIAN_LATIN_SERBIA_AND_MONTENEGRO
```


Язык: сербский (латинский, Сербия и Черногория)

### SINDHI {#SINDHI}
```
public static int SINDHI
```


Язык: синдхи

### SINDHI_DEVANAGARIC {#SINDHI-DEVANAGARIC}
```
public static int SINDHI_DEVANAGARIC
```


Язык: синдхи (Деванагари)

### SINHALESE {#SINHALESE}
```
public static int SINHALESE
```


Язык: сингальский

### SLOVAK {#SLOVAK}
```
public static int SLOVAK
```


Язык: словацкий

### SLOVENIAN {#SLOVENIAN}
```
public static int SLOVENIAN
```


Язык: словенский

### SOMALI {#SOMALI}
```
public static int SOMALI
```


Язык: сомалийский

### SORBIAN {#SORBIAN}
```
public static int SORBIAN
```


Язык: сорбский

### SPANISH_ARGENTINA {#SPANISH-ARGENTINA}
```
public static int SPANISH_ARGENTINA
```


Язык: испанский (Аргентина)

### SPANISH_BOLIVIA {#SPANISH-BOLIVIA}
```
public static int SPANISH_BOLIVIA
```


Язык: испанский (Боливия)

### SPANISH_CHILE {#SPANISH-CHILE}
```
public static int SPANISH_CHILE
```


Язык: испанский (Чили)

### SPANISH_COLOMBIA {#SPANISH-COLOMBIA}
```
public static int SPANISH_COLOMBIA
```


Язык: испанский (Колумбия)

### SPANISH_COSTA_RICA {#SPANISH-COSTA-RICA}
```
public static int SPANISH_COSTA_RICA
```


Язык: испанский (Коста-Рика)

### SPANISH_DOMINICAN_REPUBLIC {#SPANISH-DOMINICAN-REPUBLIC}
```
public static int SPANISH_DOMINICAN_REPUBLIC
```


Язык: Испанский (Доминиканская Республика)

### SPANISH_ECUADOR {#SPANISH-ECUADOR}
```
public static int SPANISH_ECUADOR
```


Язык: Испанский (Эквадор)

### SPANISH_EL_SALVADOR {#SPANISH-EL-SALVADOR}
```
public static int SPANISH_EL_SALVADOR
```


Язык: Испанский (Эль-Сальвадор)

### SPANISH_GUATEMALA {#SPANISH-GUATEMALA}
```
public static int SPANISH_GUATEMALA
```


Язык: Испанский (Гватемала)

### SPANISH_HONDURAS {#SPANISH-HONDURAS}
```
public static int SPANISH_HONDURAS
```


Язык: Испанский (Гондурас)

### SPANISH_MEXICO {#SPANISH-MEXICO}
```
public static int SPANISH_MEXICO
```


Язык: Испанский (Мексика)

### SPANISH_NICARAGUA {#SPANISH-NICARAGUA}
```
public static int SPANISH_NICARAGUA
```


Язык: Испанский (Никарагуа)

### SPANISH_PANAMA {#SPANISH-PANAMA}
```
public static int SPANISH_PANAMA
```


Язык: Испанский (Панама)

### SPANISH_PARAGUAY {#SPANISH-PARAGUAY}
```
public static int SPANISH_PARAGUAY
```


Язык: Испанский (Парагвай)

### SPANISH_PERU {#SPANISH-PERU}
```
public static int SPANISH_PERU
```


Язык: Испанский (Перу)

### SPANISH_PUERTO_RICO {#SPANISH-PUERTO-RICO}
```
public static int SPANISH_PUERTO_RICO
```


Язык: Испанский (Пуэрто-Рико)

### SPANISH_SPAIN_MODERN_SORT {#SPANISH-SPAIN-MODERN-SORT}
```
public static int SPANISH_SPAIN_MODERN_SORT
```


Язык: Испанский (Испания, современный порядок)

### SPANISH_SPAIN_TRADITIONAL_SORT {#SPANISH-SPAIN-TRADITIONAL-SORT}
```
public static int SPANISH_SPAIN_TRADITIONAL_SORT
```


Язык: Испанский (Испания, традиционный порядок)

### SPANISH_URUGUAY {#SPANISH-URUGUAY}
```
public static int SPANISH_URUGUAY
```


Язык: Испанский (Уругвай)

### SPANISH_VENEZUELA {#SPANISH-VENEZUELA}
```
public static int SPANISH_VENEZUELA
```


Язык: Испанский (Венесуэла)

### SUTU {#SUTU}
```
public static int SUTU
```


Язык: Суту

### SWEDISH_FINLAND {#SWEDISH-FINLAND}
```
public static int SWEDISH_FINLAND
```


Язык: Шведский (Финляндия)

### SWEDISH_SWEDEN {#SWEDISH-SWEDEN}
```
public static int SWEDISH_SWEDEN
```


Язык: Шведский (Швеция)

### SYRIAC {#SYRIAC}
```
public static int SYRIAC
```


Язык: Сирийский

### TAJIK {#TAJIK}
```
public static int TAJIK
```


Язык: Таджикский

### TAMAZIGHT {#TAMAZIGHT}
```
public static int TAMAZIGHT
```


Язык: Тамазигхт

### TAMAZIGHT_LATIN {#TAMAZIGHT-LATIN}
```
public static int TAMAZIGHT_LATIN
```


Язык: Тамазигхт (Латинский)

### TAMIL {#TAMIL}
```
public static int TAMIL
```


Язык: Тамильский

### TATAR {#TATAR}
```
public static int TATAR
```


Язык: Татарский

### TELUGU {#TELUGU}
```
public static int TELUGU
```


Язык: Телугу

### THAI {#THAI}
```
public static int THAI
```


Язык: Thai

### TIBETAN_BUTAN {#TIBETAN-BUTAN}
```
public static int TIBETAN_BUTAN
```


Язык: Tibetan (Bhutan)

### TIBETAN_CHINA {#TIBETAN-CHINA}
```
public static int TIBETAN_CHINA
```


Язык: Tibetan (China)

### TIGRIGNA_ERITREA {#TIGRIGNA-ERITREA}
```
public static int TIGRIGNA_ERITREA
```


Язык: Tigrigna (Eritrea)

### TIGRIGNA_ETHIOPIA {#TIGRIGNA-ETHIOPIA}
```
public static int TIGRIGNA_ETHIOPIA
```


Язык: Tigrigna (Ethiopia)

### TSONGA {#TSONGA}
```
public static int TSONGA
```


Язык: Tsonga

### TSWANA {#TSWANA}
```
public static int TSWANA
```


Язык: Tswana

### TURKISH {#TURKISH}
```
public static int TURKISH
```


Язык: Turkish

### TURKMEN {#TURKMEN}
```
public static int TURKMEN
```


Язык: Turkmen

### UKRAINIAN {#UKRAINIAN}
```
public static int UKRAINIAN
```


Язык: Ukrainian

### URDU {#URDU}
```
public static int URDU
```


Язык: Urdu

### UZBEK_CYRILLIC {#UZBEK-CYRILLIC}
```
public static int UZBEK_CYRILLIC
```


Язык: Uzbek (Cyrillic)

### UZBEK_LATIN {#UZBEK-LATIN}
```
public static int UZBEK_LATIN
```


Язык: Uzbek (Latin)

### VENDA {#VENDA}
```
public static int VENDA
```


Язык: Venda

### VIETNAMESE {#VIETNAMESE}
```
public static int VIETNAMESE
```


Язык: Vietnamese

### WELSH {#WELSH}
```
public static int WELSH
```


Язык: Welsh

### YI {#YI}
```
public static int YI
```


Язык: Yi

### YIDDISH {#YIDDISH}
```
public static int YIDDISH
```


Язык: Yiddish

### YORUBA {#YORUBA}
```
public static int YORUBA
```


Язык: Yoruba

### length {#length}
```
public static int length
```


### fromName(String editingLanguageName) {#fromName-java.lang.String}
```
public static int fromName(String editingLanguageName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| editingLanguageName | java.lang.String |  |

**Returns:**
int
### getName(int editingLanguage) {#getName-int}
```
public static String getName(int editingLanguage)
```




**Parameters:**
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
| --- | --- | --- |
| editingLanguage | int |  |

**Returns:**
java.lang.String
