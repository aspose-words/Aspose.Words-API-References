---
title: ParagraphFormat.WidowControl
second_title: Aspose.Words per .NET API Reference
description: ParagraphFormat proprietà. Vero se la prima e lultima riga del paragrafo devono rimanere sulla stessa pagina del resto del paragrafo.
type: docs
weight: 400
url: /it/net/aspose.words/paragraphformat/widowcontrol/
---
## ParagraphFormat.WidowControl property

Vero se la prima e l'ultima riga del paragrafo devono rimanere sulla stessa pagina del resto del paragrafo.

```csharp
public bool WidowControl { get; set; }
```

### Esempi

Mostra come abilitare il controllo vedova/orfano per un paragrafo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Quando scriviamo il testo che non sta in una pagina, una riga potrebbe riversarsi sulla pagina successiva.
// La singola riga che finisce nella pagina successiva è chiamata "Orfana",
// e la riga precedente in cui l'orfano si è interrotto si chiama "Vedova".
// Possiamo correggere gli orfani e le vedove riorganizzando il testo tramite la dimensione del carattere, la spaziatura o i margini della pagina.
// Se desideriamo preservare le dimensioni del nostro documento, possiamo impostare questo flag su "true"
 // per spingere le vedove sulla stessa pagina dei rispettivi orfani.
// Lasciare questo flag come "false" lascerà le coppie vedova/orfana nel testo.
// Ogni paragrafo ha questa impostazione accessibile in Microsoft Word tramite Home -> Paragrafo -> Impostazioni del paragrafo
// (pulsante nell'angolo in basso a destra della scheda "Paragrafo") -> "Controllo vedova / orfano".
builder.ParagraphFormat.WidowControl = widowControl; 

// Inserisci il testo che produce un orfano e una vedova.
builder.Font.Size = 68;
builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc.Save(ArtifactsDir + "ParagraphFormat.WidowControl.docx");
```

### Guarda anche

* class [ParagraphFormat](../)
* spazio dei nomi [Aspose.Words](../../paragraphformat/)
* assemblea [Aspose.Words](../../../)


