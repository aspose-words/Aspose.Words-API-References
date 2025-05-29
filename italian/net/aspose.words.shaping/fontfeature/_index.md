---
title: FontFeature Enum
linktitle: FontFeature
articleTitle: FontFeature
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words.Shaping.FontFeature, che descrive in dettaglio l'utilizzo dei glifi nei font per il rendering degli script. Arricchisci le tue conoscenze tipografiche oggi stesso!
type: docs
weight: 6860
url: /it/net/aspose.words.shaping/fontfeature/
---
## FontFeature enumeration

Le funzionalità forniscono informazioni su come i glifi vengono utilizzati in un font per il rendering di uno script. https://docs.microsoft.com/en-us/typography/opentype/spec/featuretags

```csharp
public enum FontFeature
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| GlyphCompositionDecomposition | `1667460464` | Per ridurre al minimo il numero di alternative di glifi, a volte è opportuno scomporre il glifo predefinito per un carattere in due o più glifi. Inoltre, potrebbe essere preferibile comporre i glifi predefiniti per due o più caratteri in un singolo glifo per una migliore elaborazione dei glifi. Questa funzionalità consente tale composizione/scomposizione. https://docs.microsoft.com/en-us/typography/opentype/spec/features_ae#ccmp Tag OpenType equivalente: 'ccmp' |
| StandardLigatures | `1818847073` | Sostituisce una sequenza di glifi con un singolo glifo, preferito per scopi tipografici. Questa funzionalità riguarda le legature che il progettista/produttore ritiene debbano essere utilizzate in condizioni normali. Tag OpenType equivalente: 'liga' https://docs.microsoft.com/en-us/typography/opentype/spec/features_ko#liga |
| RequiredLigatures | `1919707495` | Sostituisce una sequenza di glifi con un singolo glifo, preferito per scopi tipografici. Questa funzionalità riguarda le legature che lo script determina come necessarie da utilizzare in condizioni normali. Questa funzionalità è importante per alcuni script per garantire la corretta formazione dei glifi. https://docs.microsoft.com/en-us/typography/opentype/spec/features_pt#rlig Tag OpenType equivalente: 'rlig' |
| ContextualLigatures | `1668049255` | Sostituisce una sequenza di glifi con un singolo glifo, preferito per scopi tipografici. A differenza di altre funzionalità di legatura, 'clig' specifica il contesto in cui la legatura è consigliata. Questa capacità è importante in alcuni progetti di script e per le legature svolazzanti. https://docs.microsoft.com/en-us/typography/opentype/spec/features_ae#clig Tag OpenType equivalente: 'clig' |
| DiscretionaryLigatures | `1684826471` | Sostituisce una sequenza di glifi con un singolo glifo, preferito per scopi tipografici. Questa funzionalità riguarda le legature che possono essere utilizzate per effetti speciali, a discrezione dell'utente. https://docs.microsoft.com/en-us/typography/opentype/spec/features_ae#dlig Tag OpenType equivalente: 'dlig' |
| HistoricalLigatures | `1751935335` | Alcune legature erano di uso comune in passato, ma oggi appaiono anacronistiche. Alcuni font includono le forme storiche come alternative, in modo da poterle utilizzare per un effetto "d'epoca". Questa funzionalità sostituisce le forme predefinite (correnti) con le alternative storiche. https://docs.microsoft.com/en-us/typography/opentype/spec/features_fj#hlig Tag OpenType equivalente: 'hlig' |
| ProportionalFigures | `1886287213` | Sostituisce i glifi delle figure impostati su larghezze uniformi (tabulari) con i glifi corrispondenti impostati su larghezze specifiche del glifo (proporzionali). https://docs.microsoft.com/en-us/typography/opentype/spec/features_pt#tag-pnum Tag OpenType equivalente: 'pnum' |
| TabularFigures | `1953396077` | Sostituisce i glifi delle figure impostati su larghezze proporzionali con i glifi corrispondenti impostati su larghezze uniformi (tabulari). Le larghezze tabulari saranno generalmente quelle predefinite, ma non è possibile darne per scontato. Naturalmente questa funzionalità non sarà presente nei design a spaziatura fissa. https://docs.microsoft.com/en-us/typography/opentype/spec/features_pt#tag-tnum Tag OpenType equivalente: 'tnum' |
| LiningFigures | `1819178349` | Questa funzionalità trasforma le figure non allineate selezionate in figure allineate. https://docs.microsoft.com/en-us/typography/opentype/spec/features_ko#lnum Tag OpenType equivalente: 'lnum' |
| OldstyleFigures | `1869509997` | Questa funzionalità modifica le figure selezionate dallo stile predefinito o lineare al formato oldstyle. https://docs.microsoft.com/en-us/typography/opentype/spec/features_ko#onum Tag OpenType equivalente: 'onum' |
| VerticalAlternates | `1986359924` | Trasforma i glifi predefiniti in glifi adatti alla presentazione verticale in modalità di scrittura verticale. https://docs.microsoft.com/en-us/typography/opentype/spec/features_uz#tag-vert Tag OpenType equivalente: 'vert' |
| VerticalAlternatesAndRotation | `1987212338` | Sostituisce alcuni glifi a larghezza fissa (metà, terzo o quarto di larghezza) o a larghezza proporzionale (per lo più latini o katakana) con forme adatte alla scrittura verticale (ovvero ruotate di 90 gradi in senso orario). https://docs.microsoft.com/en-us/typography/opentype/spec/features_uz#tag-vrt2 Tag OpenType equivalente: 'vrt2' |
| StylisticSet01 | `1936928817` | Set stilistico 1 Oltre a, o al posto di, alternative stilistiche di singoli glifi (vedere la funzionalità 'sale'), alcuni font possono contenere set di glifi varianti stilistiche corrispondenti a parti del set di caratteri, ad esempio più varianti per le lettere minuscole in un font latino. https://docs.microsoft.com/en-us/typography/opentype/spec/features_pt#tag-ss01---ss20 Tag OpenType equivalente: 'ss01' |
| StylisticSet02 | `1936928818` | Set stilistico 2 Tag OpenType equivalente: 'ss02' |
| StylisticSet03 | `1936928819` | Set stilistico 3 Tag OpenType equivalente: 'ss03' |
| StylisticSet04 | `1936928820` | Set stilistico 4 Tag OpenType equivalente: 'ss04' |
| StylisticSet05 | `1936928821` | Set stilistico 5 Tag OpenType equivalente: 'ss05' |
| StylisticSet06 | `1936928822` | Set stilistico 6 Tag OpenType equivalente: 'ss06' |
| StylisticSet07 | `1936928823` | Set stilistico 7 Tag OpenType equivalente: 'ss07' |
| StylisticSet08 | `1936928824` | Set stilistico 8 Tag OpenType equivalente: 'ss08' |
| StylisticSet09 | `1936928825` | Set stilistico 9 Tag OpenType equivalente: 'ss09' |
| StylisticSet10 | `1936929072` | Set stilistico 10 Tag OpenType equivalente: 'ss10' |
| StylisticSet11 | `1936929073` | Set stilistico 11 Tag OpenType equivalente: 'ss11' |
| StylisticSet12 | `1936929074` | Set stilistico 12 Tag OpenType equivalente: 'ss12' |
| StylisticSet13 | `1936929075` | Set stilistico 13 Tag OpenType equivalente: 'ss13' |
| StylisticSet14 | `1936929076` | Set stilistico 14 Tag OpenType equivalente: 'ss14' |
| StylisticSet15 | `1936929077` | Set stilistico 15 Tag OpenType equivalente: 'ss15' |
| StylisticSet16 | `1936929078` | Set stilistico 16 Tag OpenType equivalente: 'ss16' |
| StylisticSet17 | `1936929079` | Set stilistico 17 Tag OpenType equivalente: 'ss17' |
| StylisticSet18 | `1936929080` | Set stilistico 18 Tag OpenType equivalente: 'ss18' |
| StylisticSet19 | `1936929081` | Set stilistico 19 Tag OpenType equivalente: 'ss19' |
| StylisticSet20 | `1936929328` | Set stilistico 20 Tag OpenType equivalente: 'ss20' |
| Kerning | `1801810542` | Regola la quantità di spazio tra i glifi, in genere per fornire una spaziatura otticamente coerente tra di essi. Sebbene un carattere ben progettato abbia una spaziatura tra i glifi complessivamente coerente, alcune combinazioni di glifi richiedono una regolazione per migliorare la leggibilità. Oltre alla regolazione standard nella direzione orizzontale, questa funzionalità può fornire dati di crenatura dipendenti dalle dimensioni tramite tabelle dei dispositivi, crenatura "cross-stream" nella direzione del testo Y e regolazione del posizionamento dei glifi indipendentemente dalla regolazione anticipata. Si noti che questa funzionalità potrebbe essere applicata a sequenze di più di due glifi e non verrebbe utilizzata nei font a spaziatura fissa. Si noti inoltre che questa funzionalità non si applica al testo disposto verticalmente. https://docs.microsoft.com/en-us/typography/opentype/spec/features_ko#kern Tag OpenType equivalente: 'kern' |

### Guarda anche

* spazio dei nomi [Aspose.Words.Shaping](../../aspose.words.shaping/)
* assemblea [Aspose.Words](../../)
