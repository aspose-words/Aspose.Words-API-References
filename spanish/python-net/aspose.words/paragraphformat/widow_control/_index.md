---
title: ParagraphFormat.widow_control property
linktitle: widow_control property
articleTitle: widow_control property
second_title: Aspose.Words for Python
description: "ParagraphFormat.widow_control property. True if the first and last lines in the paragraph are to remain on the same page as the rest of the paragraph."
type: docs
weight: 410
url: /es/python-net/aspose.words/paragraphformat/widow_control/
---

## ParagraphFormat.widow_control property

True if the first and last lines in the paragraph are to remain on the same page as the rest of the paragraph.


```python
@property
def widow_control(self) -> bool:
    ...

@widow_control.setter
def widow_control(self, value: bool):
    ...

```

### Examples

Shows how to enable widow/orphan control for a paragraph.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Cuando escribimos el texto que no cabe en una página, una línea puede desbordarse a la página siguiente.
# La única línea que termina en la página siguiente se llama "Orphan",
# y la línea anterior donde se rompe el huérfano se llama "Widow".
# Podemos corregir huérfanos y viudas reorganizando el texto mediante el tamaño de fuente, el espaciado o los márgenes de página.
# Si deseamos preservar las dimensiones de nuestro documento, podemos establecer esta bandera a "true"
# para mover las viudas a la misma página que sus respectivos huérfanos.
# Dejar esta bandera en "false" dejará pares de viuda/huérfano en el texto.
# Cada párrafo tiene esta configuración accesible en Microsoft Word a través de Inicio -> Párrafo -> Configuración de párrafo
# (botón en la esquina inferior derecha de la pestaña "Paragraph") -> "Widow/Orphan control".
builder.paragraph_format.widow_control = widow_control
# Inserte texto que produzca un huérfano y una viuda.
builder.font.size = 68
builder.write('Lorem ipsum dolor sit amet, consectetur adipiscing elit, ' + 'sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.')
doc.save(file_name=ARTIFACTS_DIR + 'ParagraphFormat.WidowControl.docx')
```

### See Also

* module [aspose.words](../../)
* class [ParagraphFormat](../)

