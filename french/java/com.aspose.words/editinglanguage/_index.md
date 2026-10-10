---
title: "EditingLanguage"
linktitle: "EditingLanguage"
second_title: "Aspose.Words pour Java"
description: "Spécifie la langue d’édition en Java."
type: docs
weight: 182
url: /fr/java/com.aspose.words/editinglanguage/
---

**Inheritance:**
java.lang.Object
```
public class EditingLanguage
```

Spécifie la langue d'édition.

 **Examples:** 

Montre comment appliquer les préférences de langue lors du chargement d’un document.

```

 LoadOptions loadOptions = new LoadOptions();
 loadOptions.getLanguagePreferences().addEditingLanguage(EditingLanguage.JAPANESE);

 Document doc = new Document(getMyDir() + "No default editing language.docx", loadOptions);

 int localeIdFarEast = doc.getStyles().getDefaultFont().getLocaleIdFarEast();
 System.out.println(localeIdFarEast == EditingLanguage.JAPANESE
         ? "The document either has no any FarEast language set in defaults or it was set to Japanese originally."
         : "The document default FarEast language was set to another than Japanese language originally, so it is not overridden.");
 
```
## Champs

| Champ | Description |
| --- | --- |
| [AFRIKAANS](#AFRIKAANS) | Langue : Afrikaans |
| [ALBANIAN](#ALBANIAN) | Langue : Albanais |
| [ALSATIAN](#ALSATIAN) | Langue : Alsacien |
| [AMHARIC](#AMHARIC) | Langue : Amharique |
| [ARABIC_ALGERIA](#ARABIC-ALGERIA) | Langue : Arabe (Algérie) |
| [ARABIC_BAHRAIN](#ARABIC-BAHRAIN) | Langue : Arabe (Bahreïn) |
| [ARABIC_EGYPT](#ARABIC-EGYPT) | Langue : Arabe (Égypte) |
| [ARABIC_IRAQ](#ARABIC-IRAQ) | Langue : Arabe (Irak) |
| [ARABIC_JORDAN](#ARABIC-JORDAN) | Langue : Arabe (Jordanie) |
| [ARABIC_KUWAIT](#ARABIC-KUWAIT) | Langue : Arabe (Koweït) |
| [ARABIC_LEBANON](#ARABIC-LEBANON) | Langue : Arabe (Liban) |
| [ARABIC_LIBYA](#ARABIC-LIBYA) | Langue : Arabe (Libye) |
| [ARABIC_MOROCCO](#ARABIC-MOROCCO) | Langue : Arabe (Maroc) |
| [ARABIC_OMAN](#ARABIC-OMAN) | Langue : Arabe (Oman) |
| [ARABIC_QATAR](#ARABIC-QATAR) | Langue : Arabe (Qatar) |
| [ARABIC_SAUDI_ARABIA](#ARABIC-SAUDI-ARABIA) | Langue : Arabe (Arabie Saoudite) |
| [ARABIC_SYRIA](#ARABIC-SYRIA) | Langue : Arabe (Syrie) |
| [ARABIC_TUNISIA](#ARABIC-TUNISIA) | Langue : Arabe (Tunisie) |
| [ARABIC_UAE](#ARABIC-UAE) | Langue : Arabe (Émirats arabes unis) |
| [ARABIC_YEMEN](#ARABIC-YEMEN) | Langue : Arabe (Yémen) |
| [ARMENIAN](#ARMENIAN) | Langue : Arménien |
| [ASSAMESE](#ASSAMESE) | Langue : Assamais |
| [AZERBAIJANI_CYRILLIC](#AZERBAIJANI-CYRILLIC) | Langue : Azerbaïdjanais (cyrillique) |
| [AZERBAIJANI_LATIN](#AZERBAIJANI-LATIN) | Langue : Azerbaïdjanais (latin) |
| [BANGLA_BANGLADESH](#BANGLA-BANGLADESH) | Langue : Bengali (Bangladesh) |
| [BANGLA_INDIA](#BANGLA-INDIA) | Langue : Bengali (Inde) |
| [BASHKIR](#BASHKIR) | Langue : Bachkir |
| [BASQUE](#BASQUE) | Langue : Basque |
| [BELARUSIAN](#BELARUSIAN) | Langue : Biélorusse |
| [BOSNIAN_CYRILLIC](#BOSNIAN-CYRILLIC) | Langue : Bosniaque (cyrillique) |
| [BOSNIAN_LATIN](#BOSNIAN-LATIN) | Langue : Bosniaque (latin) |
| [BRETON](#BRETON) | Langue : Breton |
| [BULGARIAN](#BULGARIAN) | Langue : Bulgare |
| [BURMESE](#BURMESE) | Langue: Birman |
| [CATALAN](#CATALAN) | Langue: Catalan |
| [CENTRAL_KURDISH_IRAQ](#CENTRAL-KURDISH-IRAQ) | Langue: Kurde central (Irak) |
| [CHEROKEE](#CHEROKEE) | Langue: Cherokee |
| [CHINESE_HONG_KONG](#CHINESE-HONG-KONG) | Langue: Chinois (Hong Kong) |
| [CHINESE_MACAO](#CHINESE-MACAO) | Langue: Chinois (Macao) |
| [CHINESE_PRC](#CHINESE-PRC) | Langue: Chinois (RPC) |
| [CHINESE_SINGAPORE](#CHINESE-SINGAPORE) | Langue: Chinois (Singapour) |
| [CHINESE_TAIWAN](#CHINESE-TAIWAN) | Langue: Chinois (Taïwan) |
| [CORSICAN](#CORSICAN) | Langue: Corse |
| [CROATIAN](#CROATIAN) | Langue: Croate |
| [CROATIAN_BOZNIA_AND_HERZEGOVINA](#CROATIAN-BOZNIA-AND-HERZEGOVINA) | Langue: Croate (Bosnie-Herzégovine) |
| [CZECH](#CZECH) | Langue: Tchèque |
| [DANISH](#DANISH) | Langue: Danois |
| [DIVEHI](#DIVEHI) | Langue: Divehi |
| [DUTCH_BELGIUM](#DUTCH-BELGIUM) | Langue: Néerlandais (Belgique) |
| [DUTCH_NETHERLANDS](#DUTCH-NETHERLANDS) | Langue: Néerlandais (Pays-Bas) |
| [EDO](#EDO) | Langue: Édo |
| [ENGLISH_AUSTRALIA](#ENGLISH-AUSTRALIA) | Langue: Anglais (Australie) |
| [ENGLISH_BELIZE](#ENGLISH-BELIZE) | Langue: Anglais (Belize) |
| [ENGLISH_CANADA](#ENGLISH-CANADA) | Langue: Anglais (Canada) |
| [ENGLISH_CARIBBEAN](#ENGLISH-CARIBBEAN) | Langue: Anglais (Caraïbes) |
| [ENGLISH_HONG_KONG](#ENGLISH-HONG-KONG) | Langue: Anglais (Hong Kong) |
| [ENGLISH_INDIA](#ENGLISH-INDIA) | Langue: Anglais (Inde) |
| [ENGLISH_INDONESIA](#ENGLISH-INDONESIA) | Langue: Anglais (Indonésie) |
| [ENGLISH_IRELAND](#ENGLISH-IRELAND) | Langue : Anglais (Irlande) |
| [ENGLISH_JAMAICA](#ENGLISH-JAMAICA) | Langue : Anglais (Jamaïque) |
| [ENGLISH_MALAYSIA](#ENGLISH-MALAYSIA) | Langue : Anglais (Malaisie) |
| [ENGLISH_NEW_ZEALAND](#ENGLISH-NEW-ZEALAND) | Langue : Anglais (Nouvelle-Zélande) |
| [ENGLISH_PHILIPPINES](#ENGLISH-PHILIPPINES) | Langue : Anglais (Philippines) |
| [ENGLISH_SINGAPORE](#ENGLISH-SINGAPORE) | Langue : Anglais (Singapour) |
| [ENGLISH_SOUTH_AFRICA](#ENGLISH-SOUTH-AFRICA) | Langue : Anglais (Afrique du Sud) |
| [ENGLISH_TRINIDAD_AND_TOBAGO](#ENGLISH-TRINIDAD-AND-TOBAGO) | Langue : Anglais (Trinité-et-Tobago) |
| [ENGLISH_UK](#ENGLISH-UK) | Langue : Anglais (Royaume-Uni) |
| [ENGLISH_US](#ENGLISH-US) | Langue : Anglais (États-Unis) |
| [ENGLISH_ZIMBABWE](#ENGLISH-ZIMBABWE) | Langue : Anglais (Zimbabwe) |
| [ESTONIAN](#ESTONIAN) | Langue : Estonien |
| [FAEROESE](#FAEROESE) | Langue : Féroïen |
| [FILIPINO](#FILIPINO) | Langue : Filipino |
| [FINNISH](#FINNISH) | Langue : Finnois |
| [FRENCH_BELGIUM](#FRENCH-BELGIUM) | Langue : Français (Belgique) |
| [FRENCH_CANADA](#FRENCH-CANADA) | Langue : Français (Canada) |
| [FRENCH_FRANCE](#FRENCH-FRANCE) | Langue : Français (France) |
| [FRENCH_LUXEMBOURG](#FRENCH-LUXEMBOURG) | Langue : Français (Luxembourg) |
| [FRENCH_MONACO](#FRENCH-MONACO) | Langue : Français (Monaco) |
| [FRENCH_SWITZERLAND](#FRENCH-SWITZERLAND) | Langue : Français (Suisse) |
| [FRISIAN](#FRISIAN) | Langue : Frison |
| [FULAH_LATIN_SENEGAL](#FULAH-LATIN-SENEGAL) | Langue : Peul (Latin, Sénégal) |
| [FULAH_NIGERIA](#FULAH-NIGERIA) | Langue : Peul (Nigeria) |
| [GALICIAN](#GALICIAN) | Langue : Galicien |
| [GEORGIAN](#GEORGIAN) | Langue : Géorgien |
| [GERMAN_AUSTRIA](#GERMAN-AUSTRIA) | Langue : Allemand (Autriche) |
| [GERMAN_GERMANY](#GERMAN-GERMANY) | Langue : Allemand (Allemagne) |
| [GERMAN_LIECHTENSTEIN](#GERMAN-LIECHTENSTEIN) | Langue : Allemand (Liechtenstein) |
| [GERMAN_LUXEMBOURG](#GERMAN-LUXEMBOURG) | Langue : Allemand (Luxembourg) |
| [GERMAN_SWITZERLAND](#GERMAN-SWITZERLAND) | Langue : Allemand (Suisse) |
| [GREEK](#GREEK) | Langue : Grec |
| [GREENLANDIC](#GREENLANDIC) | Langue : Groenlandais |
| [GUARANI](#GUARANI) | Langue : Guarani |
| [GUJARATI](#GUJARATI) | Langue : Gujarati |
| [HAUSA](#HAUSA) | Langue : Hausa |
| [HAWAIIAN](#HAWAIIAN) | Langue : Hawaïen |
| [HEBREW](#HEBREW) | Langue : Hébreu |
| [HINDI](#HINDI) | Langue : Hindi |
| [HUNGARIAN](#HUNGARIAN) | Langue : Hongrois |
| [ICELANDIC](#ICELANDIC) | Langue : Islandais |
| [IGBO](#IGBO) | Langue : Igbo |
| [INARI_SAMI_FINLAND](#INARI-SAMI-FINLAND) | Langue : Sami d'Inari (Finlande) |
| [INDONESIAN](#INDONESIAN) | Langue : Indonésien |
| [INUKTITUT_LATIN](#INUKTITUT-LATIN) | Langue : Inuktitut (Latin) |
| [INUKTITUT_SYLLABICS](#INUKTITUT-SYLLABICS) | Langue : Inuktitut (Syllabiques) |
| [IRISH](#IRISH) | Langue : Irlandais |
| [ISI_XHOSA](#ISI-XHOSA) | Langue : isiXhosa |
| [ISI_ZULU](#ISI-ZULU) | Langue : isiZulu |
| [ITALIAN_ITALY](#ITALIAN-ITALY) | Langue : Italien (Italie) |
| [ITALIAN_SWITZERLAND](#ITALIAN-SWITZERLAND) | Langue : italien (Suisse) |
| [JAPANESE](#JAPANESE) | Langue : japonais |
| [KANNADA](#KANNADA) | Langue : kannada |
| [KANURI](#KANURI) | Langue : kanouri |
| [KASHMIRI](#KASHMIRI) | Langue : cachemiri |
| [KASHMIRI_ARABIC](#KASHMIRI-ARABIC) | Langue : cachemiri (arabe) |
| [KAZAKH](#KAZAKH) | Langue : kazakh |
| [KHMER](#KHMER) | Langue : khmer |
| [KICHE](#KICHE) | Langue : k'iche |
| [KINYARWANDA](#KINYARWANDA) | Langue : kinyarwanda |
| [KISWAHILI](#KISWAHILI) | Langue : swahili |
| [KONKANI](#KONKANI) | Langue : konkani |
| [KOREAN](#KOREAN) | Langue : coréen |
| [KYRGYZ](#KYRGYZ) | Langue : kirghize |
| [LAO](#LAO) | Langue : lao |
| [LATIN](#LATIN) | Langue : latin |
| [LATVIAN](#LATVIAN) | Langue : letton |
| [LITHUANIAN](#LITHUANIAN) | Langue : lituanien |
| [LOWER_SORBIAN](#LOWER-SORBIAN) | Langue : sorabe inférieur |
| [LULE_SAMI_NORWAY](#LULE-SAMI-NORWAY) | Langue : sami de Lule (Norvège) |
| [LULE_SAMI_SWEDEN](#LULE-SAMI-SWEDEN) | Langue : sami de Lule (Suède) |
| [LUXEMBOUGISH](#LUXEMBOUGISH) | Langue : luxembourgeois |
| [MACEDONIAN](#MACEDONIAN) | Langue : macédonien |
| [MALAYALAM](#MALAYALAM) | Langue : malayalam |
| [MALAY_BRUNEI_DARUSSALAM](#MALAY-BRUNEI-DARUSSALAM) | Langue : malais (Brunei Darussalam) |
| [MALAY_MALAYSIA](#MALAY-MALAYSIA) | Langue: malais (Malaisie) |
| [MALTESE](#MALTESE) | Langue: maltais |
| [MANIPURI](#MANIPURI) | Langue: manipuri |
| [MAORI](#MAORI) | Langue: maori |
| [MAPUDUNGUN_CHILE](#MAPUDUNGUN-CHILE) | Langue: mapudungun (Chili) |
| [MARATHI](#MARATHI) | Langue: marathi |
| [MOHAWK](#MOHAWK) | Langue: mohawk |
| [MONGOLIAN_CYRILLIC](#MONGOLIAN-CYRILLIC) | Langue: mongol (cyrillique) |
| [MONGOLIAN_MONGOLIAN](#MONGOLIAN-MONGOLIAN) | Langue: mongol (mongol) |
| [NEPALI](#NEPALI) | Langue: népalais |
| [NORTHERN_SAMI_FINLAND](#NORTHERN-SAMI-FINLAND) | Langue: Sami du Nord (Finlande) |
| [NORTHERN_SAMI_NORWAY](#NORTHERN-SAMI-NORWAY) | Langue: Sami du Nord (Norvège) |
| [NORTHERN_SAMI_SWEDEN](#NORTHERN-SAMI-SWEDEN) | Langue: Sami du Nord (Suède) |
| [NORWEGIAN_BOKMAL](#NORWEGIAN-BOKMAL) | Langue: norvégien bokmål |
| [NORWEGIAN_NYNORSK](#NORWEGIAN-NYNORSK) | Langue: norvégien nynorsk |
| [ORIYA](#ORIYA) | Langue: oriya |
| [OROMO](#OROMO) | Langue: oromo |
| [PAPIAMENTU](#PAPIAMENTU) | Langue: papiamento |
| [PASHTO](#PASHTO) | Langue: pachto |
| [PERSIAN](#PERSIAN) | Langue: persan |
| [POLISH](#POLISH) | Langue: polonais |
| [PORTUGUESE_BRAZIL](#PORTUGUESE-BRAZIL) | Langue: portugais (Brésil) |
| [PORTUGUESE_PORTUGAL](#PORTUGUESE-PORTUGAL) | Langue: portugais (Portugal) |
| [PUNJABI_INDIA](#PUNJABI-INDIA) | Langue: pendjabi (Inde) |
| [PUNJABI_PAKISTAN](#PUNJABI-PAKISTAN) | Langue: pendjabi (Pakistan) |
| [QUECHUA_BOLIVIA](#QUECHUA-BOLIVIA) | Langue : Quechua (Bolivie) |
| [QUECHUA_ECUADOR](#QUECHUA-ECUADOR) | Langue : Quechua (Équateur) |
| [QUECHUA_PERU](#QUECHUA-PERU) | Langue : Quechua (Pérou) |
| [ROMANIAN](#ROMANIAN) | Langue : Roumain |
| [ROMANSH](#ROMANSH) | Langue : Romanche |
| [RUSSIAN](#RUSSIAN) | Langue : Russe |
| [SAKHA](#SAKHA) | Langue : Sakha |
| [SANSKRIT](#SANSKRIT) | Langue : Sanskrit |
| [SCOTTISH_GAELIC](#SCOTTISH-GAELIC) | Langue : Gaélique écossais |
| [SERBIAN_CYRILLIC_BOSNIA_AND_HERZEGOVINA](#SERBIAN-CYRILLIC-BOSNIA-AND-HERZEGOVINA) | Langue : Serbe (cyrillique, Bosnie-Herzégovine) |
| [SERBIAN_CYRILLIC_SERBIA_AND_MONTENEGRO](#SERBIAN-CYRILLIC-SERBIA-AND-MONTENEGRO) | Langue : Serbe (cyrillique, Serbie-et-Monténégro) |
| [SERBIAN_LATIN_BOSNIA_AND_HERZEGOVINA](#SERBIAN-LATIN-BOSNIA-AND-HERZEGOVINA) | Langue : Serbe (latin, Bosnie-Herzégovine) |
| [SERBIAN_LATIN_SERBIA_AND_MONTENEGRO](#SERBIAN-LATIN-SERBIA-AND-MONTENEGRO) | Langue : Serbe (latin, Serbie-et-Monténégro) |
| [SINDHI](#SINDHI) | Langue : Sindhi |
| [SINDHI_DEVANAGARIC](#SINDHI-DEVANAGARIC) | Langue : Sindhi (Devanagari) |
| [SINHALESE](#SINHALESE) | Langue : Cingalais |
| [SLOVAK](#SLOVAK) | Langue : Slovaque |
| [SLOVENIAN](#SLOVENIAN) | Langue : Slovène |
| [SOMALI](#SOMALI) | Langue : Somalien |
| [SORBIAN](#SORBIAN) | Langue : Sorabe |
| [SPANISH_ARGENTINA](#SPANISH-ARGENTINA) | Langue : Espagnol (Argentine) |
| [SPANISH_BOLIVIA](#SPANISH-BOLIVIA) | Langue : Espagnol (Bolivie) |
| [SPANISH_CHILE](#SPANISH-CHILE) | Langue : Espagnol (Chili) |
| [SPANISH_COLOMBIA](#SPANISH-COLOMBIA) | Langue : Espagnol (Colombie) |
| [SPANISH_COSTA_RICA](#SPANISH-COSTA-RICA) | Langue : Espagnol (Costa Rica) |
| [SPANISH_DOMINICAN_REPUBLIC](#SPANISH-DOMINICAN-REPUBLIC) | Langue : espagnol (République dominicaine) |
| [SPANISH_ECUADOR](#SPANISH-ECUADOR) | Langue : espagnol (Équateur) |
| [SPANISH_EL_SALVADOR](#SPANISH-EL-SALVADOR) | Langue : espagnol (Salvador) |
| [SPANISH_GUATEMALA](#SPANISH-GUATEMALA) | Langue : espagnol (Guatemala) |
| [SPANISH_HONDURAS](#SPANISH-HONDURAS) | Langue : espagnol (Honduras) |
| [SPANISH_MEXICO](#SPANISH-MEXICO) | Langue : espagnol (Mexique) |
| [SPANISH_NICARAGUA](#SPANISH-NICARAGUA) | Langue : espagnol (Nicaragua) |
| [SPANISH_PANAMA](#SPANISH-PANAMA) | Langue : espagnol (Panama) |
| [SPANISH_PARAGUAY](#SPANISH-PARAGUAY) | Langue : espagnol (Paraguay) |
| [SPANISH_PERU](#SPANISH-PERU) | Langue : espagnol (Pérou) |
| [SPANISH_PUERTO_RICO](#SPANISH-PUERTO-RICO) | Langue : espagnol (Porto Rico) |
| [SPANISH_SPAIN_MODERN_SORT](#SPANISH-SPAIN-MODERN-SORT) | Langue : espagnol (Espagne, tri moderne) |
| [SPANISH_SPAIN_TRADITIONAL_SORT](#SPANISH-SPAIN-TRADITIONAL-SORT) | Langue : espagnol (Espagne, tri traditionnel) |
| [SPANISH_URUGUAY](#SPANISH-URUGUAY) | Langue : espagnol (Uruguay) |
| [SPANISH_VENEZUELA](#SPANISH-VENEZUELA) | Langue : espagnol (Venezuela) |
| [SUTU](#SUTU) | Langue : sutu |
| [SWEDISH_FINLAND](#SWEDISH-FINLAND) | Langue : suédois (Finlande) |
| [SWEDISH_SWEDEN](#SWEDISH-SWEDEN) | Langue : suédois (Suède) |
| [SYRIAC](#SYRIAC) | Langue : syriaque |
| [TAJIK](#TAJIK) | Langue : tadjik |
| [TAMAZIGHT](#TAMAZIGHT) | Langue : tamazight |
| [TAMAZIGHT_LATIN](#TAMAZIGHT-LATIN) | Langue : tamazight (latin) |
| [TAMIL](#TAMIL) | Langue : tamoul |
| [TATAR](#TATAR) | Langue : tatar |
| [TELUGU](#TELUGU) | Langue : télougou |
| [THAI](#THAI) | Langue : Thai |
| [TIBETAN_BUTAN](#TIBETAN-BUTAN) | Langue : Tibetan (Bhutan) |
| [TIBETAN_CHINA](#TIBETAN-CHINA) | Langue : Tibetan (China) |
| [TIGRIGNA_ERITREA](#TIGRIGNA-ERITREA) | Langue : Tigrigna (Eritrea) |
| [TIGRIGNA_ETHIOPIA](#TIGRIGNA-ETHIOPIA) | Langue : Tigrigna (Ethiopia) |
| [TSONGA](#TSONGA) | Langue : Tsonga |
| [TSWANA](#TSWANA) | Langue : Tswana |
| [TURKISH](#TURKISH) | Langue : Turkish |
| [TURKMEN](#TURKMEN) | Langue : Turkmen |
| [UKRAINIAN](#UKRAINIAN) | Langue : Ukrainian |
| [URDU](#URDU) | Langue : Urdu |
| [UZBEK_CYRILLIC](#UZBEK-CYRILLIC) | Langue : Uzbek (Cyrillic) |
| [UZBEK_LATIN](#UZBEK-LATIN) | Langue : Uzbek (Latin) |
| [VENDA](#VENDA) | Langue : Venda |
| [VIETNAMESE](#VIETNAMESE) | Langue : Vietnamese |
| [WELSH](#WELSH) | Langue : Welsh |
| [YI](#YI) | Langue : Yi |
| [YIDDISH](#YIDDISH) | Langue : Yiddish |
| [YORUBA](#YORUBA) | Langue : Yoruba |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String editingLanguageName)](#fromName-java.lang.String) |  |
| [getName(int editingLanguage)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int editingLanguage)](#toString-int) |  |
### AFRIKAANS {#AFRIKAANS}
```
public static int AFRIKAANS
```


Langue : Afrikaans

### ALBANIAN {#ALBANIAN}
```
public static int ALBANIAN
```


Langue : Albanais

### ALSATIAN {#ALSATIAN}
```
public static int ALSATIAN
```


Langue : Alsacien

### AMHARIC {#AMHARIC}
```
public static int AMHARIC
```


Langue : Amharique

### ARABIC_ALGERIA {#ARABIC-ALGERIA}
```
public static int ARABIC_ALGERIA
```


Langue : Arabe (Algérie)

### ARABIC_BAHRAIN {#ARABIC-BAHRAIN}
```
public static int ARABIC_BAHRAIN
```


Langue : Arabe (Bahreïn)

### ARABIC_EGYPT {#ARABIC-EGYPT}
```
public static int ARABIC_EGYPT
```


Langue : Arabe (Égypte)

### ARABIC_IRAQ {#ARABIC-IRAQ}
```
public static int ARABIC_IRAQ
```


Langue : Arabe (Irak)

### ARABIC_JORDAN {#ARABIC-JORDAN}
```
public static int ARABIC_JORDAN
```


Langue : Arabe (Jordanie)

### ARABIC_KUWAIT {#ARABIC-KUWAIT}
```
public static int ARABIC_KUWAIT
```


Langue : Arabe (Koweït)

### ARABIC_LEBANON {#ARABIC-LEBANON}
```
public static int ARABIC_LEBANON
```


Langue : Arabe (Liban)

### ARABIC_LIBYA {#ARABIC-LIBYA}
```
public static int ARABIC_LIBYA
```


Langue : Arabe (Libye)

### ARABIC_MOROCCO {#ARABIC-MOROCCO}
```
public static int ARABIC_MOROCCO
```


Langue : Arabe (Maroc)

### ARABIC_OMAN {#ARABIC-OMAN}
```
public static int ARABIC_OMAN
```


Langue : Arabe (Oman)

### ARABIC_QATAR {#ARABIC-QATAR}
```
public static int ARABIC_QATAR
```


Langue : Arabe (Qatar)

### ARABIC_SAUDI_ARABIA {#ARABIC-SAUDI-ARABIA}
```
public static int ARABIC_SAUDI_ARABIA
```


Langue : Arabe (Arabie Saoudite)

### ARABIC_SYRIA {#ARABIC-SYRIA}
```
public static int ARABIC_SYRIA
```


Langue : Arabe (Syrie)

### ARABIC_TUNISIA {#ARABIC-TUNISIA}
```
public static int ARABIC_TUNISIA
```


Langue : Arabe (Tunisie)

### ARABIC_UAE {#ARABIC-UAE}
```
public static int ARABIC_UAE
```


Langue : Arabe (Émirats arabes unis)

### ARABIC_YEMEN {#ARABIC-YEMEN}
```
public static int ARABIC_YEMEN
```


Langue : Arabe (Yémen)

### ARMENIAN {#ARMENIAN}
```
public static int ARMENIAN
```


Langue : Arménien

### ASSAMESE {#ASSAMESE}
```
public static int ASSAMESE
```


Langue : Assamais

### AZERBAIJANI_CYRILLIC {#AZERBAIJANI-CYRILLIC}
```
public static int AZERBAIJANI_CYRILLIC
```


Langue : Azerbaïdjanais (cyrillique)

### AZERBAIJANI_LATIN {#AZERBAIJANI-LATIN}
```
public static int AZERBAIJANI_LATIN
```


Langue : Azerbaïdjanais (latin)

### BANGLA_BANGLADESH {#BANGLA-BANGLADESH}
```
public static int BANGLA_BANGLADESH
```


Langue : Bengali (Bangladesh)

### BANGLA_INDIA {#BANGLA-INDIA}
```
public static int BANGLA_INDIA
```


Langue : Bengali (Inde)

### BASHKIR {#BASHKIR}
```
public static int BASHKIR
```


Langue : Bachkir

### BASQUE {#BASQUE}
```
public static int BASQUE
```


Langue : Basque

### BELARUSIAN {#BELARUSIAN}
```
public static int BELARUSIAN
```


Langue : Biélorusse

### BOSNIAN_CYRILLIC {#BOSNIAN-CYRILLIC}
```
public static int BOSNIAN_CYRILLIC
```


Langue : Bosniaque (cyrillique)

### BOSNIAN_LATIN {#BOSNIAN-LATIN}
```
public static int BOSNIAN_LATIN
```


Langue : Bosniaque (latin)

### BRETON {#BRETON}
```
public static int BRETON
```


Langue : Breton

### BULGARIAN {#BULGARIAN}
```
public static int BULGARIAN
```


Langue : Bulgare

### BURMESE {#BURMESE}
```
public static int BURMESE
```


Langue: Birman

### CATALAN {#CATALAN}
```
public static int CATALAN
```


Langue: Catalan

### CENTRAL_KURDISH_IRAQ {#CENTRAL-KURDISH-IRAQ}
```
public static int CENTRAL_KURDISH_IRAQ
```


Langue: Kurde central (Irak)

### CHEROKEE {#CHEROKEE}
```
public static int CHEROKEE
```


Langue: Cherokee

### CHINESE_HONG_KONG {#CHINESE-HONG-KONG}
```
public static int CHINESE_HONG_KONG
```


Langue: Chinois (Hong Kong)

### CHINESE_MACAO {#CHINESE-MACAO}
```
public static int CHINESE_MACAO
```


Langue: Chinois (Macao)

### CHINESE_PRC {#CHINESE-PRC}
```
public static int CHINESE_PRC
```


Langue: Chinois (RPC)

### CHINESE_SINGAPORE {#CHINESE-SINGAPORE}
```
public static int CHINESE_SINGAPORE
```


Langue: Chinois (Singapour)

### CHINESE_TAIWAN {#CHINESE-TAIWAN}
```
public static int CHINESE_TAIWAN
```


Langue: Chinois (Taïwan)

### CORSICAN {#CORSICAN}
```
public static int CORSICAN
```


Langue: Corse

### CROATIAN {#CROATIAN}
```
public static int CROATIAN
```


Langue: Croate

### CROATIAN_BOZNIA_AND_HERZEGOVINA {#CROATIAN-BOZNIA-AND-HERZEGOVINA}
```
public static int CROATIAN_BOZNIA_AND_HERZEGOVINA
```


Langue: Croate (Bosnie-Herzégovine)

### CZECH {#CZECH}
```
public static int CZECH
```


Langue: Tchèque

### DANISH {#DANISH}
```
public static int DANISH
```


Langue: Danois

### DIVEHI {#DIVEHI}
```
public static int DIVEHI
```


Langue: Divehi

### DUTCH_BELGIUM {#DUTCH-BELGIUM}
```
public static int DUTCH_BELGIUM
```


Langue: Néerlandais (Belgique)

### DUTCH_NETHERLANDS {#DUTCH-NETHERLANDS}
```
public static int DUTCH_NETHERLANDS
```


Langue: Néerlandais (Pays-Bas)

### EDO {#EDO}
```
public static int EDO
```


Langue: Édo

### ENGLISH_AUSTRALIA {#ENGLISH-AUSTRALIA}
```
public static int ENGLISH_AUSTRALIA
```


Langue: Anglais (Australie)

### ENGLISH_BELIZE {#ENGLISH-BELIZE}
```
public static int ENGLISH_BELIZE
```


Langue: Anglais (Belize)

### ENGLISH_CANADA {#ENGLISH-CANADA}
```
public static int ENGLISH_CANADA
```


Langue: Anglais (Canada)

### ENGLISH_CARIBBEAN {#ENGLISH-CARIBBEAN}
```
public static int ENGLISH_CARIBBEAN
```


Langue: Anglais (Caraïbes)

### ENGLISH_HONG_KONG {#ENGLISH-HONG-KONG}
```
public static int ENGLISH_HONG_KONG
```


Langue: Anglais (Hong Kong)

### ENGLISH_INDIA {#ENGLISH-INDIA}
```
public static int ENGLISH_INDIA
```


Langue: Anglais (Inde)

### ENGLISH_INDONESIA {#ENGLISH-INDONESIA}
```
public static int ENGLISH_INDONESIA
```


Langue: Anglais (Indonésie)

### ENGLISH_IRELAND {#ENGLISH-IRELAND}
```
public static int ENGLISH_IRELAND
```


Langue : Anglais (Irlande)

### ENGLISH_JAMAICA {#ENGLISH-JAMAICA}
```
public static int ENGLISH_JAMAICA
```


Langue : Anglais (Jamaïque)

### ENGLISH_MALAYSIA {#ENGLISH-MALAYSIA}
```
public static int ENGLISH_MALAYSIA
```


Langue : Anglais (Malaisie)

### ENGLISH_NEW_ZEALAND {#ENGLISH-NEW-ZEALAND}
```
public static int ENGLISH_NEW_ZEALAND
```


Langue : Anglais (Nouvelle-Zélande)

### ENGLISH_PHILIPPINES {#ENGLISH-PHILIPPINES}
```
public static int ENGLISH_PHILIPPINES
```


Langue : Anglais (Philippines)

### ENGLISH_SINGAPORE {#ENGLISH-SINGAPORE}
```
public static int ENGLISH_SINGAPORE
```


Langue : Anglais (Singapour)

### ENGLISH_SOUTH_AFRICA {#ENGLISH-SOUTH-AFRICA}
```
public static int ENGLISH_SOUTH_AFRICA
```


Langue : Anglais (Afrique du Sud)

### ENGLISH_TRINIDAD_AND_TOBAGO {#ENGLISH-TRINIDAD-AND-TOBAGO}
```
public static int ENGLISH_TRINIDAD_AND_TOBAGO
```


Langue : Anglais (Trinité-et-Tobago)

### ENGLISH_UK {#ENGLISH-UK}
```
public static int ENGLISH_UK
```


Langue : Anglais (Royaume-Uni)

### ENGLISH_US {#ENGLISH-US}
```
public static int ENGLISH_US
```


Langue : Anglais (États-Unis)

### ENGLISH_ZIMBABWE {#ENGLISH-ZIMBABWE}
```
public static int ENGLISH_ZIMBABWE
```


Langue : Anglais (Zimbabwe)

### ESTONIAN {#ESTONIAN}
```
public static int ESTONIAN
```


Langue : Estonien

### FAEROESE {#FAEROESE}
```
public static int FAEROESE
```


Langue : Féroïen

### FILIPINO {#FILIPINO}
```
public static int FILIPINO
```


Langue : Filipino

### FINNISH {#FINNISH}
```
public static int FINNISH
```


Langue : Finnois

### FRENCH_BELGIUM {#FRENCH-BELGIUM}
```
public static int FRENCH_BELGIUM
```


Langue : Français (Belgique)

### FRENCH_CANADA {#FRENCH-CANADA}
```
public static int FRENCH_CANADA
```


Langue : Français (Canada)

### FRENCH_FRANCE {#FRENCH-FRANCE}
```
public static int FRENCH_FRANCE
```


Langue : Français (France)

### FRENCH_LUXEMBOURG {#FRENCH-LUXEMBOURG}
```
public static int FRENCH_LUXEMBOURG
```


Langue : Français (Luxembourg)

### FRENCH_MONACO {#FRENCH-MONACO}
```
public static int FRENCH_MONACO
```


Langue : Français (Monaco)

### FRENCH_SWITZERLAND {#FRENCH-SWITZERLAND}
```
public static int FRENCH_SWITZERLAND
```


Langue : Français (Suisse)

### FRISIAN {#FRISIAN}
```
public static int FRISIAN
```


Langue : Frison

### FULAH_LATIN_SENEGAL {#FULAH-LATIN-SENEGAL}
```
public static int FULAH_LATIN_SENEGAL
```


Langue : Peul (Latin, Sénégal)

### FULAH_NIGERIA {#FULAH-NIGERIA}
```
public static int FULAH_NIGERIA
```


Langue : Peul (Nigeria)

### GALICIAN {#GALICIAN}
```
public static int GALICIAN
```


Langue : Galicien

### GEORGIAN {#GEORGIAN}
```
public static int GEORGIAN
```


Langue : Géorgien

### GERMAN_AUSTRIA {#GERMAN-AUSTRIA}
```
public static int GERMAN_AUSTRIA
```


Langue : Allemand (Autriche)

### GERMAN_GERMANY {#GERMAN-GERMANY}
```
public static int GERMAN_GERMANY
```


Langue : Allemand (Allemagne)

### GERMAN_LIECHTENSTEIN {#GERMAN-LIECHTENSTEIN}
```
public static int GERMAN_LIECHTENSTEIN
```


Langue : Allemand (Liechtenstein)

### GERMAN_LUXEMBOURG {#GERMAN-LUXEMBOURG}
```
public static int GERMAN_LUXEMBOURG
```


Langue : Allemand (Luxembourg)

### GERMAN_SWITZERLAND {#GERMAN-SWITZERLAND}
```
public static int GERMAN_SWITZERLAND
```


Langue : Allemand (Suisse)

### GREEK {#GREEK}
```
public static int GREEK
```


Langue : Grec

### GREENLANDIC {#GREENLANDIC}
```
public static int GREENLANDIC
```


Langue : Groenlandais

### GUARANI {#GUARANI}
```
public static int GUARANI
```


Langue : Guarani

### GUJARATI {#GUJARATI}
```
public static int GUJARATI
```


Langue : Gujarati

### HAUSA {#HAUSA}
```
public static int HAUSA
```


Langue : Hausa

### HAWAIIAN {#HAWAIIAN}
```
public static int HAWAIIAN
```


Langue : Hawaïen

### HEBREW {#HEBREW}
```
public static int HEBREW
```


Langue : Hébreu

### HINDI {#HINDI}
```
public static int HINDI
```


Langue : Hindi

### HUNGARIAN {#HUNGARIAN}
```
public static int HUNGARIAN
```


Langue : Hongrois

### ICELANDIC {#ICELANDIC}
```
public static int ICELANDIC
```


Langue : Islandais

### IGBO {#IGBO}
```
public static int IGBO
```


Langue : Igbo

### INARI_SAMI_FINLAND {#INARI-SAMI-FINLAND}
```
public static int INARI_SAMI_FINLAND
```


Langue : Sami d'Inari (Finlande)

### INDONESIAN {#INDONESIAN}
```
public static int INDONESIAN
```


Langue : Indonésien

### INUKTITUT_LATIN {#INUKTITUT-LATIN}
```
public static int INUKTITUT_LATIN
```


Langue : Inuktitut (Latin)

### INUKTITUT_SYLLABICS {#INUKTITUT-SYLLABICS}
```
public static int INUKTITUT_SYLLABICS
```


Langue : Inuktitut (Syllabiques)

### IRISH {#IRISH}
```
public static int IRISH
```


Langue : Irlandais

### ISI_XHOSA {#ISI-XHOSA}
```
public static int ISI_XHOSA
```


Langue : isiXhosa

### ISI_ZULU {#ISI-ZULU}
```
public static int ISI_ZULU
```


Langue : isiZulu

### ITALIAN_ITALY {#ITALIAN-ITALY}
```
public static int ITALIAN_ITALY
```


Langue : Italien (Italie)

### ITALIAN_SWITZERLAND {#ITALIAN-SWITZERLAND}
```
public static int ITALIAN_SWITZERLAND
```


Langue : italien (Suisse)

### JAPANESE {#JAPANESE}
```
public static int JAPANESE
```


Langue : japonais

### KANNADA {#KANNADA}
```
public static int KANNADA
```


Langue : kannada

### KANURI {#KANURI}
```
public static int KANURI
```


Langue : kanouri

### KASHMIRI {#KASHMIRI}
```
public static int KASHMIRI
```


Langue : cachemiri

### KASHMIRI_ARABIC {#KASHMIRI-ARABIC}
```
public static int KASHMIRI_ARABIC
```


Langue : cachemiri (arabe)

### KAZAKH {#KAZAKH}
```
public static int KAZAKH
```


Langue : kazakh

### KHMER {#KHMER}
```
public static int KHMER
```


Langue : khmer

### KICHE {#KICHE}
```
public static int KICHE
```


Langue : k'iche

### KINYARWANDA {#KINYARWANDA}
```
public static int KINYARWANDA
```


Langue : kinyarwanda

### KISWAHILI {#KISWAHILI}
```
public static int KISWAHILI
```


Langue : swahili

### KONKANI {#KONKANI}
```
public static int KONKANI
```


Langue : konkani

### KOREAN {#KOREAN}
```
public static int KOREAN
```


Langue : coréen

### KYRGYZ {#KYRGYZ}
```
public static int KYRGYZ
```


Langue : kirghize

### LAO {#LAO}
```
public static int LAO
```


Langue : lao

### LATIN {#LATIN}
```
public static int LATIN
```


Langue : latin

### LATVIAN {#LATVIAN}
```
public static int LATVIAN
```


Langue : letton

### LITHUANIAN {#LITHUANIAN}
```
public static int LITHUANIAN
```


Langue : lituanien

### LOWER_SORBIAN {#LOWER-SORBIAN}
```
public static int LOWER_SORBIAN
```


Langue : sorabe inférieur

### LULE_SAMI_NORWAY {#LULE-SAMI-NORWAY}
```
public static int LULE_SAMI_NORWAY
```


Langue : sami de Lule (Norvège)

### LULE_SAMI_SWEDEN {#LULE-SAMI-SWEDEN}
```
public static int LULE_SAMI_SWEDEN
```


Langue : sami de Lule (Suède)

### LUXEMBOUGISH {#LUXEMBOUGISH}
```
public static int LUXEMBOUGISH
```


Langue : luxembourgeois

### MACEDONIAN {#MACEDONIAN}
```
public static int MACEDONIAN
```


Langue : macédonien

### MALAYALAM {#MALAYALAM}
```
public static int MALAYALAM
```


Langue : malayalam

### MALAY_BRUNEI_DARUSSALAM {#MALAY-BRUNEI-DARUSSALAM}
```
public static int MALAY_BRUNEI_DARUSSALAM
```


Langue : malais (Brunei Darussalam)

### MALAY_MALAYSIA {#MALAY-MALAYSIA}
```
public static int MALAY_MALAYSIA
```


Langue: malais (Malaisie)

### MALTESE {#MALTESE}
```
public static int MALTESE
```


Langue: maltais

### MANIPURI {#MANIPURI}
```
public static int MANIPURI
```


Langue: manipuri

### MAORI {#MAORI}
```
public static int MAORI
```


Langue: maori

### MAPUDUNGUN_CHILE {#MAPUDUNGUN-CHILE}
```
public static int MAPUDUNGUN_CHILE
```


Langue: mapudungun (Chili)

### MARATHI {#MARATHI}
```
public static int MARATHI
```


Langue: marathi

### MOHAWK {#MOHAWK}
```
public static int MOHAWK
```


Langue: mohawk

### MONGOLIAN_CYRILLIC {#MONGOLIAN-CYRILLIC}
```
public static int MONGOLIAN_CYRILLIC
```


Langue: mongol (cyrillique)

### MONGOLIAN_MONGOLIAN {#MONGOLIAN-MONGOLIAN}
```
public static int MONGOLIAN_MONGOLIAN
```


Langue: mongol (mongol)

### NEPALI {#NEPALI}
```
public static int NEPALI
```


Langue: népalais

### NORTHERN_SAMI_FINLAND {#NORTHERN-SAMI-FINLAND}
```
public static int NORTHERN_SAMI_FINLAND
```


Langue: Sami du Nord (Finlande)

### NORTHERN_SAMI_NORWAY {#NORTHERN-SAMI-NORWAY}
```
public static int NORTHERN_SAMI_NORWAY
```


Langue: Sami du Nord (Norvège)

### NORTHERN_SAMI_SWEDEN {#NORTHERN-SAMI-SWEDEN}
```
public static int NORTHERN_SAMI_SWEDEN
```


Langue: Sami du Nord (Suède)

### NORWEGIAN_BOKMAL {#NORWEGIAN-BOKMAL}
```
public static int NORWEGIAN_BOKMAL
```


Langue: norvégien bokmål

### NORWEGIAN_NYNORSK {#NORWEGIAN-NYNORSK}
```
public static int NORWEGIAN_NYNORSK
```


Langue: norvégien nynorsk

### ORIYA {#ORIYA}
```
public static int ORIYA
```


Langue: oriya

### OROMO {#OROMO}
```
public static int OROMO
```


Langue: oromo

### PAPIAMENTU {#PAPIAMENTU}
```
public static int PAPIAMENTU
```


Langue: papiamento

### PASHTO {#PASHTO}
```
public static int PASHTO
```


Langue: pachto

### PERSIAN {#PERSIAN}
```
public static int PERSIAN
```


Langue: persan

### POLISH {#POLISH}
```
public static int POLISH
```


Langue: polonais

### PORTUGUESE_BRAZIL {#PORTUGUESE-BRAZIL}
```
public static int PORTUGUESE_BRAZIL
```


Langue: portugais (Brésil)

### PORTUGUESE_PORTUGAL {#PORTUGUESE-PORTUGAL}
```
public static int PORTUGUESE_PORTUGAL
```


Langue: portugais (Portugal)

### PUNJABI_INDIA {#PUNJABI-INDIA}
```
public static int PUNJABI_INDIA
```


Langue: pendjabi (Inde)

### PUNJABI_PAKISTAN {#PUNJABI-PAKISTAN}
```
public static int PUNJABI_PAKISTAN
```


Langue: pendjabi (Pakistan)

### QUECHUA_BOLIVIA {#QUECHUA-BOLIVIA}
```
public static int QUECHUA_BOLIVIA
```


Langue : Quechua (Bolivie)

### QUECHUA_ECUADOR {#QUECHUA-ECUADOR}
```
public static int QUECHUA_ECUADOR
```


Langue : Quechua (Équateur)

### QUECHUA_PERU {#QUECHUA-PERU}
```
public static int QUECHUA_PERU
```


Langue : Quechua (Pérou)

### ROMANIAN {#ROMANIAN}
```
public static int ROMANIAN
```


Langue : Roumain

### ROMANSH {#ROMANSH}
```
public static int ROMANSH
```


Langue : Romanche

### RUSSIAN {#RUSSIAN}
```
public static int RUSSIAN
```


Langue : Russe

### SAKHA {#SAKHA}
```
public static int SAKHA
```


Langue : Sakha

### SANSKRIT {#SANSKRIT}
```
public static int SANSKRIT
```


Langue : Sanskrit

### SCOTTISH_GAELIC {#SCOTTISH-GAELIC}
```
public static int SCOTTISH_GAELIC
```


Langue : Gaélique écossais

### SERBIAN_CYRILLIC_BOSNIA_AND_HERZEGOVINA {#SERBIAN-CYRILLIC-BOSNIA-AND-HERZEGOVINA}
```
public static int SERBIAN_CYRILLIC_BOSNIA_AND_HERZEGOVINA
```


Langue : Serbe (cyrillique, Bosnie-Herzégovine)

### SERBIAN_CYRILLIC_SERBIA_AND_MONTENEGRO {#SERBIAN-CYRILLIC-SERBIA-AND-MONTENEGRO}
```
public static int SERBIAN_CYRILLIC_SERBIA_AND_MONTENEGRO
```


Langue : Serbe (cyrillique, Serbie-et-Monténégro)

### SERBIAN_LATIN_BOSNIA_AND_HERZEGOVINA {#SERBIAN-LATIN-BOSNIA-AND-HERZEGOVINA}
```
public static int SERBIAN_LATIN_BOSNIA_AND_HERZEGOVINA
```


Langue : Serbe (latin, Bosnie-Herzégovine)

### SERBIAN_LATIN_SERBIA_AND_MONTENEGRO {#SERBIAN-LATIN-SERBIA-AND-MONTENEGRO}
```
public static int SERBIAN_LATIN_SERBIA_AND_MONTENEGRO
```


Langue : Serbe (latin, Serbie-et-Monténégro)

### SINDHI {#SINDHI}
```
public static int SINDHI
```


Langue : Sindhi

### SINDHI_DEVANAGARIC {#SINDHI-DEVANAGARIC}
```
public static int SINDHI_DEVANAGARIC
```


Langue : Sindhi (Devanagari)

### SINHALESE {#SINHALESE}
```
public static int SINHALESE
```


Langue : Cingalais

### SLOVAK {#SLOVAK}
```
public static int SLOVAK
```


Langue : Slovaque

### SLOVENIAN {#SLOVENIAN}
```
public static int SLOVENIAN
```


Langue : Slovène

### SOMALI {#SOMALI}
```
public static int SOMALI
```


Langue : Somalien

### SORBIAN {#SORBIAN}
```
public static int SORBIAN
```


Langue : Sorabe

### SPANISH_ARGENTINA {#SPANISH-ARGENTINA}
```
public static int SPANISH_ARGENTINA
```


Langue : Espagnol (Argentine)

### SPANISH_BOLIVIA {#SPANISH-BOLIVIA}
```
public static int SPANISH_BOLIVIA
```


Langue : Espagnol (Bolivie)

### SPANISH_CHILE {#SPANISH-CHILE}
```
public static int SPANISH_CHILE
```


Langue : Espagnol (Chili)

### SPANISH_COLOMBIA {#SPANISH-COLOMBIA}
```
public static int SPANISH_COLOMBIA
```


Langue : Espagnol (Colombie)

### SPANISH_COSTA_RICA {#SPANISH-COSTA-RICA}
```
public static int SPANISH_COSTA_RICA
```


Langue : Espagnol (Costa Rica)

### SPANISH_DOMINICAN_REPUBLIC {#SPANISH-DOMINICAN-REPUBLIC}
```
public static int SPANISH_DOMINICAN_REPUBLIC
```


Langue : espagnol (République dominicaine)

### SPANISH_ECUADOR {#SPANISH-ECUADOR}
```
public static int SPANISH_ECUADOR
```


Langue : espagnol (Équateur)

### SPANISH_EL_SALVADOR {#SPANISH-EL-SALVADOR}
```
public static int SPANISH_EL_SALVADOR
```


Langue : espagnol (Salvador)

### SPANISH_GUATEMALA {#SPANISH-GUATEMALA}
```
public static int SPANISH_GUATEMALA
```


Langue : espagnol (Guatemala)

### SPANISH_HONDURAS {#SPANISH-HONDURAS}
```
public static int SPANISH_HONDURAS
```


Langue : espagnol (Honduras)

### SPANISH_MEXICO {#SPANISH-MEXICO}
```
public static int SPANISH_MEXICO
```


Langue : espagnol (Mexique)

### SPANISH_NICARAGUA {#SPANISH-NICARAGUA}
```
public static int SPANISH_NICARAGUA
```


Langue : espagnol (Nicaragua)

### SPANISH_PANAMA {#SPANISH-PANAMA}
```
public static int SPANISH_PANAMA
```


Langue : espagnol (Panama)

### SPANISH_PARAGUAY {#SPANISH-PARAGUAY}
```
public static int SPANISH_PARAGUAY
```


Langue : espagnol (Paraguay)

### SPANISH_PERU {#SPANISH-PERU}
```
public static int SPANISH_PERU
```


Langue : espagnol (Pérou)

### SPANISH_PUERTO_RICO {#SPANISH-PUERTO-RICO}
```
public static int SPANISH_PUERTO_RICO
```


Langue : espagnol (Porto Rico)

### SPANISH_SPAIN_MODERN_SORT {#SPANISH-SPAIN-MODERN-SORT}
```
public static int SPANISH_SPAIN_MODERN_SORT
```


Langue : espagnol (Espagne, tri moderne)

### SPANISH_SPAIN_TRADITIONAL_SORT {#SPANISH-SPAIN-TRADITIONAL-SORT}
```
public static int SPANISH_SPAIN_TRADITIONAL_SORT
```


Langue : espagnol (Espagne, tri traditionnel)

### SPANISH_URUGUAY {#SPANISH-URUGUAY}
```
public static int SPANISH_URUGUAY
```


Langue : espagnol (Uruguay)

### SPANISH_VENEZUELA {#SPANISH-VENEZUELA}
```
public static int SPANISH_VENEZUELA
```


Langue : espagnol (Venezuela)

### SUTU {#SUTU}
```
public static int SUTU
```


Langue : sutu

### SWEDISH_FINLAND {#SWEDISH-FINLAND}
```
public static int SWEDISH_FINLAND
```


Langue : suédois (Finlande)

### SWEDISH_SWEDEN {#SWEDISH-SWEDEN}
```
public static int SWEDISH_SWEDEN
```


Langue : suédois (Suède)

### SYRIAC {#SYRIAC}
```
public static int SYRIAC
```


Langue : syriaque

### TAJIK {#TAJIK}
```
public static int TAJIK
```


Langue : tadjik

### TAMAZIGHT {#TAMAZIGHT}
```
public static int TAMAZIGHT
```


Langue : tamazight

### TAMAZIGHT_LATIN {#TAMAZIGHT-LATIN}
```
public static int TAMAZIGHT_LATIN
```


Langue : tamazight (latin)

### TAMIL {#TAMIL}
```
public static int TAMIL
```


Langue : tamoul

### TATAR {#TATAR}
```
public static int TATAR
```


Langue : tatar

### TELUGU {#TELUGU}
```
public static int TELUGU
```


Langue : télougou

### THAI {#THAI}
```
public static int THAI
```


Langue : Thai

### TIBETAN_BUTAN {#TIBETAN-BUTAN}
```
public static int TIBETAN_BUTAN
```


Langue : Tibetan (Bhutan)

### TIBETAN_CHINA {#TIBETAN-CHINA}
```
public static int TIBETAN_CHINA
```


Langue : Tibetan (China)

### TIGRIGNA_ERITREA {#TIGRIGNA-ERITREA}
```
public static int TIGRIGNA_ERITREA
```


Langue : Tigrigna (Eritrea)

### TIGRIGNA_ETHIOPIA {#TIGRIGNA-ETHIOPIA}
```
public static int TIGRIGNA_ETHIOPIA
```


Langue : Tigrigna (Ethiopia)

### TSONGA {#TSONGA}
```
public static int TSONGA
```


Langue : Tsonga

### TSWANA {#TSWANA}
```
public static int TSWANA
```


Langue : Tswana

### TURKISH {#TURKISH}
```
public static int TURKISH
```


Langue : Turkish

### TURKMEN {#TURKMEN}
```
public static int TURKMEN
```


Langue : Turkmen

### UKRAINIAN {#UKRAINIAN}
```
public static int UKRAINIAN
```


Langue : Ukrainian

### URDU {#URDU}
```
public static int URDU
```


Langue : Urdu

### UZBEK_CYRILLIC {#UZBEK-CYRILLIC}
```
public static int UZBEK_CYRILLIC
```


Langue : Uzbek (Cyrillic)

### UZBEK_LATIN {#UZBEK-LATIN}
```
public static int UZBEK_LATIN
```


Langue : Uzbek (Latin)

### VENDA {#VENDA}
```
public static int VENDA
```


Langue : Venda

### VIETNAMESE {#VIETNAMESE}
```
public static int VIETNAMESE
```


Langue : Vietnamese

### WELSH {#WELSH}
```
public static int WELSH
```


Langue : Welsh

### YI {#YI}
```
public static int YI
```


Langue : Yi

### YIDDISH {#YIDDISH}
```
public static int YIDDISH
```


Langue : Yiddish

### YORUBA {#YORUBA}
```
public static int YORUBA
```


Langue : Yoruba

### length {#length}
```
public static int length
```


### fromName(String editingLanguageName) {#fromName-java.lang.String}
```
public static int fromName(String editingLanguageName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| editingLanguageName | java.lang.String |  |

**Returns:**
int
### getName(int editingLanguage) {#getName-int}
```
public static String getName(int editingLanguage)
```




**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
| --- | --- | --- |
| editingLanguage | int |  |

**Returns:**
java.lang.String
