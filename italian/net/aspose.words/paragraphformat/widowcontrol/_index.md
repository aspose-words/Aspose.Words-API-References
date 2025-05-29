---
title: ParagraphFormat.WidowControl
linktitle: WidowControl
articleTitle: WidowControl
second_title: Aspose.Words per .NET
description: Scopri come la proprietà WidowControl ParagraphFormat garantisce che la prima e l'ultima riga del testo rimangano unite sulla stessa pagina per una migliore leggibilità.
type: docs
weight: 410
url: /it/net/aspose.words/paragraphformat/widowcontrol/
---
## ParagraphFormat.WidowControl property

Vero se la prima e l'ultima riga del paragrafo devono rimanere sulla stessa pagina del resto del paragrafo.

```csharp
public bool WidowControl { get; set; }
```

## Esempi

Mostra come abilitare il controllo vedove/orfani per un paragrafo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Quando scriviamo un testo che non entra in una pagina, una riga potrebbe fuoriuscire dalla pagina successiva.
// La singola riga che finisce nella pagina successiva si chiama "Orfano",
// e la riga precedente in cui l'orfano si è interrotto si chiama "Vedova".
// Possiamo risolvere i problemi relativi a orfani e vedove riorganizzando il testo tramite la dimensione del carattere, la spaziatura o i margini della pagina.
// Se vogliamo preservare le dimensioni del nostro documento, possiamo impostare questo flag su "true"
// per mettere le vedove sulla stessa lunghezza d'onda dei rispettivi orfani.
// Lasciando questo flag su "false" verranno lasciate le coppie vedova/orfano nel testo.
// Ogni paragrafo ha questa impostazione accessibile in Microsoft Word tramite Home -> Paragrafo -> Impostazioni paragrafo
// (pulsante nell'angolo in basso a destra della scheda "Paragrafo") -> "Controllo vedove/orfani".
builder.ParagraphFormat.WidowControl = widowControl; 

// Inserire testo che genera un orfano e una vedova.
builder.Font.Size = 68;
builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc.Save(ArtifactsDir + "ParagraphFormat.WidowControl.docx");
```

### Guarda anche

* class [ParagraphFormat](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
