---
title: "Clase Aspose::Words::Settings::CompatibilityOptions"
linktitle: "CompatibilityOptions"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Clase Aspose::Words::Settings::CompatibilityOptions. Contiene opciones de compatibilidad (es decir, las preferencias del usuario ingresadas en la pestaña Compatibilidad del cuadro de diálogo Opciones en Microsoft Word). Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 1000
url: /es/cpp/aspose.words.settings/compatibilityoptions/
---
## CompatibilityOptions class


Contiene opciones de compatibilidad (es decir, las preferencias del usuario ingresadas en la pestaña **Compatibility** del cuadro de diálogo **Options** en Microsoft Word). Para obtener más información, visite el artículo de documentación [Detect File Format and Check Format Compatibility](https://docs.aspose.com/words/cpp/detect-file-format-and-check-format-compatibility/).

```cpp
class CompatibilityOptions : public System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [get_AdjustLineHeightInTable](./get_adjustlineheightintable/)() | Agregar el paso de línea de cuadrícula de [Document](../../aspose.words/document/) a las líneas en celdas de tabla. |
| [get_AlignTablesRowByRow](./get_aligntablesrowbyrow/)() | Alinear filas de tabla de forma independiente. |
| [get_AllowSpaceOfSameStyleInTable](./get_allowspaceofsamestyleintable/)() | Permitir espaciado contextual de párrafos en [Tables](../../aspose.words.tables/). |
| [get_ApplyBreakingRules](./get_applybreakingrules/)() | Utilizar reglas de salto de línea heredadas para etíope y amárico. |
| [get_AutofitToFirstFixedWidthCell](./get_autofittofirstfixedwidthcell/)() | Permitir que las columnas de tabla excedan los anchos preferidos de las celdas constituyentes. |
| [get_AutoSpaceLikeWord95](./get_autospacelikeword95/)() | Emular el espaciado de caracteres de ancho completo de Word 95. |
| [get_BalanceSingleByteDoubleByteWidth](./get_balancesinglebytedoublebytewidth/)() | Equilibrar caracteres de un solo byte y de doble byte. |
| [get_CachedColBalance](./get_cachedcolbalance/)() | Utilizar información en caché de [Paragraph](../../aspose.words/paragraph/) para el equilibrio de columnas. |
| [get_ConvMailMergeEsc](./get_convmailmergeesc/)() | Tratar el delimitador de comillas de barra invertida como dos comillas. |
| [get_DisableOpenTypeFontFormattingFeatures](./get_disableopentypefontformattingfeatures/)() | Especifica desactivar las funciones de formato de fuentes OpenType. |
| [get_DisplayHangulFixedWidth](./get_displayhangulfixedwidth/)() | Usar siempre ancho fijo para caracteres Hangul. |
| [get_DoNotAutofitConstrainedTables](./get_donotautofitconstrainedtables/)() | No ajustar automáticamente [Tables](../../aspose.words.tables/) para que encajen junto a objetos envueltos. |
| [get_DoNotBreakConstrainedForcedTable](./get_donotbreakconstrainedforcedtable/)() | No romper filas de tabla alrededor de [Tables](../../aspose.words.tables/) flotantes. |
| [get_DoNotBreakWrappedTables](./get_donotbreakwrappedtables/)() | No permitir que [Tables](../../aspose.words.tables/) flotantes se dividan entre páginas. |
| [get_DoNotExpandShiftReturn](./get_donotexpandshiftreturn/)() | No justificar líneas que terminan en salto de línea suave. |
| [get_DoNotLeaveBackslashAlone](./get_donotleavebackslashalone/)() | Convertir la barra invertida a signo de yen al ingresarla. |
| [get_DoNotSnapToGridInCell](./get_donotsnaptogridincell/)() | No ajustar a la cuadrícula de [Document](../../aspose.words/document/) en celdas de tabla con objetos. |
| [get_DoNotSuppressIndentation](./get_donotsuppressindentation/)() | No ignorar objetos flotantes al calcular la sangría de [Paragraph](../../aspose.words/paragraph/). |
| [get_DoNotSuppressParagraphBorders](./get_donotsuppressparagraphborders/)() | No suprimir los bordes del [Paragraph](../../aspose.words/paragraph/) junto a los marcos. |
| [get_DoNotUseEastAsianBreakRules](./get_donotuseeastasianbreakrules/)() | No comprimir los caracteres comprimibles al usar la cuadrícula del [Document](../../aspose.words/document/). |
| [get_DoNotUseHTMLParagraphAutoSpacing](./get_donotusehtmlparagraphautospacing/)() | Usar espaciado fijo del [Paragraph](../../aspose.words/paragraph/) para la configuración automática de HTML. |
| [get_DoNotUseIndentAsNumberingTabStop](./get_donotuseindentasnumberingtabstop/)() | Ignorar sangría colgante al crear una tabulación después de la numeración. |
| [get_DoNotVertAlignCellWithSp](./get_donotvertaligncellwithsp/)() | No alinear verticalmente celdas que contienen objetos flotantes. |
| [get_DoNotVertAlignInTxbx](./get_donotvertalignintxbx/)() | Ignorar la alineación vertical en los cuadros de texto. |
| [get_DoNotWrapTextWithPunct](./get_donotwraptextwithpunct/)() | No permitir puntuación colgante con la cuadrícula de caracteres. |
| [get_FootnoteLayoutLikeWW8](./get_footnotelayoutlikeww8/)() | Emular la ubicación de notas al pie de Word 6.x/95/97. |
| [get_ForgetLastTabAlignment](./get_forgetlasttabalignment/)() | Ignorar el ancho de la última tabulación al alinear el [Paragraph](../../aspose.words/paragraph/) si no está alineado a la izquierda. |
| [get_GrowAutofit](./get_growautofit/)() | Permitir que las [Tables](../../aspose.words.tables/) se ajusten automáticamente a los márgenes de la página. |
| [get_LayoutRawTableWidth](./get_layoutrawtablewidth/)() | Ignorar el espacio antes de la tabla al decidir si la tabla debe envolver un objeto flotante. |
| [get_LayoutTableRowsApart](./get_layouttablerowsapart/)() | Permitir que las filas de la tabla envuelvan objetos [Inline](../../aspose.words/inline/) de forma independiente. |
| [get_LineWrapLikeWord6](./get_linewraplikeword6/)() | Emular el ajuste de línea de Word 6.0 para texto de Asia oriental. |
| [get_MWSmallCaps](./get_mwsmallcaps/)() | Emular Word 5.x para el formato de versalitas en Macintosh. |
| [get_NoColumnBalance](./get_nocolumnbalance/)() | No equilibrar columnas de texto dentro de una [Section](../../aspose.words/section/). |
| [get_NoExtraLineSpacing](./get_noextralinespacing/)() | No centrar el contenido en líneas con altura de línea exacta. |
| [get_NoLeading](./get_noleading/)() | No añadir interlineado entre líneas de texto. |
| [get_NoSpaceRaiseLower](./get_nospaceraiselower/)() | No aumentar la altura de línea para texto elevado/bajado. |
| [get_NoTabHangInd](./get_notabhangind/)() | No crear una tabulación personalizada para sangría colgante. |
| [get_OverrideTableStyleFontSizeAndJustification](./get_overridetablestylefontsizeandjustification/)() | Especifica cómo se evalúa la jerarquía de estilos del documento. |
| [get_PrintBodyTextBeforeHeader](./get_printbodytextbeforeheader/)() | Imprimir el texto del [Body](../../aspose.words/body/) antes del contenido del encabezado/pie de página. |
| [get_PrintColBlack](./get_printcolblack/)() | Imprimir colores en blanco y negro sin tramado. |
| [get_SelectFldWithFirstOrLastChar](./get_selectfldwithfirstorlastchar/)() | Seleccionar campo cuando se selecciona el primer o último carácter. |
| [get_ShapeLayoutLikeWW8](./get_shapelayoutlikeww8/)() | Emular el ajuste de texto de Word 97 alrededor de objetos flotantes. |
| [get_ShowBreaksInFrames](./get_showbreaksinframes/)() | Mostrar saltos de página/columna presentes en los marcos. |
| [get_SpaceForUL](./get_spaceforul/)() | Agregar espacio adicional debajo de la línea base para texto asiático oriental subrayado. |
| [get_SpacingInWholePoints](./get_spacinginwholepoints/)() | Solo expandir/contraer texto por puntos completos. |
| [get_SplitPgBreakAndParaMark](./get_splitpgbreakandparamark/)() | Siempre mover la marca de [Paragraph](../../aspose.words/paragraph/) a la página después de un salto de página. |
| [get_SubFontBySize](./get_subfontbysize/)() | Incrementar la prioridad del tamaño de [Font](../../aspose.words/font/) durante la sustitución de [Font](../../aspose.words/font/). |
| [get_SuppressBottomSpacing](./get_suppressbottomspacing/)() | Ignorar la altura exacta de línea para la última línea en la página. |
| [get_SuppressSpacingAtTopOfPage](./get_suppressspacingattopofpage/)() | Ignorar la altura mínima de línea para la primera línea en la página. |
| [get_SuppressSpBfAfterPgBrk](./get_suppressspbfafterpgbrk/)() | No usar espacio antes en la primera línea después de un salto de página. |
| [get_SuppressTopSpacing](./get_suppresstopspacing/)() | Ignorar la altura mínima y exacta de línea para la primera línea en la página. |
| [get_SuppressTopSpacingWP](./get_suppresstopspacingwp/)() | Emular el interlineado de WordPerfect 5.x. |
| [get_SwapBordersFacingPgs](./get_swapbordersfacingpgs/)() | Intercambiar los bordes de [Paragraph](../../aspose.words/paragraph/) en páginas impares. |
| [get_SwapInsideAndOutsideForMirrorIndentsAndRelativePositioning](./get_swapinsideandoutsideformirrorindentsandrelativepositioning/)() | Especifica intercambiar interior y exterior para sangrías espejo y posicionamiento relativo. |
| [get_TransparentMetafiles](./get_transparentmetafiles/)() | Especifica no dejar en blanco el área detrás de imágenes metafile. |
| [get_TruncateFontHeightsLikeWP6](./get_truncatefontheightslikewp6/)() | Emular el cálculo de altura de [Font](../../aspose.words/font/) en WordPerfect 6.x. |
| [get_UICompat97To2003](./get_uicompat97to2003/)() | Verdadero para desactivar la funcionalidad de la UI que no es compatible con Word97-2003. El valor predeterminado es **false**. |
| [get_UlTrailSpace](./get_ultrailspace/)() | Subrayar todos los espacios finales. |
| [get_UnderlineTabInNumList](./get_underlinetabinnumlist/)() | Subrayar el carácter siguiente después de la numeración. |
| [get_UseAltKinsokuLineBreakRules](./get_usealtkinsokulinebreakrules/)() | Usar conjunto alternativo de reglas de salto de línea para asiático oriental. |
| [get_UseAnsiKerningPairs](./get_useansikerningpairs/)() | Usar pares de kerning ANSI de [Fonts](../../aspose.words.fonts/). |
| [get_UseFELayout](./get_usefelayout/)() | No omitir el código de [Layout](../../aspose.words.layout/) para asiático oriental/escritura compleja. |
| [get_UseNormalStyleForList](./get_usenormalstyleforlist/)() | No aplicar automáticamente la [Paragraph](../../aspose.words/paragraph/)[Style](../../aspose.words/style/) de lista al texto con viñetas/numerado. |
| [get_UsePrinterMetrics](./get_useprintermetrics/)() | Usar métricas de impresora para mostrar documentos. |
| [get_UseSingleBorderforContiguousCells](./get_usesingleborderforcontiguouscells/)() | Usar reglas simplificadas para conflictos de [Border](../../aspose.words/border/) de tabla. |
| [get_UseWord2002TableStyleRules](./get_useword2002tablestylerules/)() | Emular las reglas de [Style](../../aspose.words/style/) de tabla de Word 2002. |
| [get_UseWord2010TableStyleRules](./get_useword2010tablestylerules/)() | Especifica usar reglas de estilo de tabla de Word2010. |
| [get_UseWord97LineBreakRules](./get_useword97linebreakrules/)() | Emular el salto de línea de asiático oriental de Word 97. |
| [get_WPJustification](./get_wpjustification/)() | Emular WordPerfect 6.x [Paragraph](../../aspose.words/paragraph/) Justificación. |
| [get_WPSpaceWidth](./get_wpspacewidth/)() | Especifica si se debe establecer el ancho de un espacio como se hace en WordPerfect 5.x. |
| [get_WrapTrailSpaces](./get_wraptrailspaces/)() | Ajuste de línea de espacios finales. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [OptimizeFor](./optimizefor/)(Aspose::Words::Settings::MsWordVersion) | Permite optimizar el contenido del documento así como el comportamiento predeterminado de Aspose.Words para versiones particulares de MS Word. Utilice este método para evitar que MS Word muestre la cinta "Compatibility mode" al cargar el documento. (Nota: también puede ser necesario establecer la propiedad [Compliance](../../aspose.words.saving/ooxmlsaveoptions/get_compliance/) a [Iso29500_2008_Transitional](../../aspose.words.saving/ooxmlcompliance/) o superior.) |
| [set_AdjustLineHeightInTable](./set_adjustlineheightintable/)(bool) | Agregar el paso de línea de cuadrícula de [Document](../../aspose.words/document/) a las líneas en celdas de tabla. |
| [set_AlignTablesRowByRow](./set_aligntablesrowbyrow/)(bool) | Alinear filas de tabla de forma independiente. |
| [set_AllowSpaceOfSameStyleInTable](./set_allowspaceofsamestyleintable/)(bool) | Permitir espaciado contextual de párrafos en [Tables](../../aspose.words.tables/). |
| [set_ApplyBreakingRules](./set_applybreakingrules/)(bool) | Utilizar reglas de salto de línea heredadas para etíope y amárico. |
| [set_AutofitToFirstFixedWidthCell](./set_autofittofirstfixedwidthcell/)(bool) | Permitir que las columnas de tabla excedan los anchos preferidos de las celdas constituyentes. |
| [set_AutoSpaceLikeWord95](./set_autospacelikeword95/)(bool) | Emular el espaciado de caracteres de ancho completo de Word 95. |
| [set_BalanceSingleByteDoubleByteWidth](./set_balancesinglebytedoublebytewidth/)(bool) | Equilibrar caracteres de un solo byte y de doble byte. |
| [set_CachedColBalance](./set_cachedcolbalance/)(bool) | Utilizar información en caché de [Paragraph](../../aspose.words/paragraph/) para el equilibrio de columnas. |
| [set_ConvMailMergeEsc](./set_convmailmergeesc/)(bool) | Tratar el delimitador de comillas de barra invertida como dos comillas. |
| [set_DisableOpenTypeFontFormattingFeatures](./set_disableopentypefontformattingfeatures/)(bool) | Especifica desactivar las funciones de formato de fuentes OpenType. |
| [set_DisplayHangulFixedWidth](./set_displayhangulfixedwidth/)(bool) | Usar siempre ancho fijo para caracteres Hangul. |
| [set_DoNotAutofitConstrainedTables](./set_donotautofitconstrainedtables/)(bool) | No ajustar automáticamente [Tables](../../aspose.words.tables/) para que encajen junto a objetos envueltos. |
| [set_DoNotBreakConstrainedForcedTable](./set_donotbreakconstrainedforcedtable/)(bool) | No romper filas de tabla alrededor de [Tables](../../aspose.words.tables/) flotantes. |
| [set_DoNotBreakWrappedTables](./set_donotbreakwrappedtables/)(bool) | No permitir que [Tables](../../aspose.words.tables/) flotantes se dividan entre páginas. |
| [set_DoNotExpandShiftReturn](./set_donotexpandshiftreturn/)(bool) | No justificar líneas que terminan en salto de línea suave. |
| [set_DoNotLeaveBackslashAlone](./set_donotleavebackslashalone/)(bool) | Convertir la barra invertida a signo de yen al ingresarla. |
| [set_DoNotSnapToGridInCell](./set_donotsnaptogridincell/)(bool) | No ajustar a la cuadrícula de [Document](../../aspose.words/document/) en celdas de tabla con objetos. |
| [set_DoNotSuppressIndentation](./set_donotsuppressindentation/)(bool) | No ignorar objetos flotantes al calcular la sangría de [Paragraph](../../aspose.words/paragraph/). |
| [set_DoNotSuppressParagraphBorders](./set_donotsuppressparagraphborders/)(bool) | No suprimir los bordes del [Paragraph](../../aspose.words/paragraph/) junto a los marcos. |
| [set_DoNotUseEastAsianBreakRules](./set_donotuseeastasianbreakrules/)(bool) | No comprimir los caracteres comprimibles al usar la cuadrícula del [Document](../../aspose.words/document/). |
| [set_DoNotUseHTMLParagraphAutoSpacing](./set_donotusehtmlparagraphautospacing/)(bool) | Usar espaciado fijo del [Paragraph](../../aspose.words/paragraph/) para la configuración automática de HTML. |
| [set_DoNotUseIndentAsNumberingTabStop](./set_donotuseindentasnumberingtabstop/)(bool) | Ignorar sangría colgante al crear una tabulación después de la numeración. |
| [set_DoNotVertAlignCellWithSp](./set_donotvertaligncellwithsp/)(bool) | No alinear verticalmente celdas que contienen objetos flotantes. |
| [set_DoNotVertAlignInTxbx](./set_donotvertalignintxbx/)(bool) | Ignorar la alineación vertical en los cuadros de texto. |
| [set_DoNotWrapTextWithPunct](./set_donotwraptextwithpunct/)(bool) | No permitir puntuación colgante con la cuadrícula de caracteres. |
| [set_FootnoteLayoutLikeWW8](./set_footnotelayoutlikeww8/)(bool) | Emular la ubicación de notas al pie de Word 6.x/95/97. |
| [set_ForgetLastTabAlignment](./set_forgetlasttabalignment/)(bool) | Ignorar el ancho de la última tabulación al alinear el [Paragraph](../../aspose.words/paragraph/) si no está alineado a la izquierda. |
| [set_GrowAutofit](./set_growautofit/)(bool) | Permitir que las [Tables](../../aspose.words.tables/) se ajusten automáticamente a los márgenes de la página. |
| [set_LayoutRawTableWidth](./set_layoutrawtablewidth/)(bool) | Ignorar el espacio antes de la tabla al decidir si la tabla debe envolver un objeto flotante. |
| [set_LayoutTableRowsApart](./set_layouttablerowsapart/)(bool) | Permitir que las filas de la tabla envuelvan objetos [Inline](../../aspose.words/inline/) de forma independiente. |
| [set_LineWrapLikeWord6](./set_linewraplikeword6/)(bool) | Emular el ajuste de línea de Word 6.0 para texto de Asia oriental. |
| [set_MWSmallCaps](./set_mwsmallcaps/)(bool) | Emular Word 5.x para el formato de versalitas en Macintosh. |
| [set_NoColumnBalance](./set_nocolumnbalance/)(bool) | No equilibrar columnas de texto dentro de una [Section](../../aspose.words/section/). |
| [set_NoExtraLineSpacing](./set_noextralinespacing/)(bool) | No centrar el contenido en líneas con altura de línea exacta. |
| [set_NoLeading](./set_noleading/)(bool) | No añadir interlineado entre líneas de texto. |
| [set_NoSpaceRaiseLower](./set_nospaceraiselower/)(bool) | No aumentar la altura de línea para texto elevado/bajado. |
| [set_NoTabHangInd](./set_notabhangind/)(bool) | No crear una tabulación personalizada para sangría colgante. |
| [set_OverrideTableStyleFontSizeAndJustification](./set_overridetablestylefontsizeandjustification/)(bool) | Especifica cómo se evalúa la jerarquía de estilos del documento. |
| [set_PrintBodyTextBeforeHeader](./set_printbodytextbeforeheader/)(bool) | Imprimir el texto del [Body](../../aspose.words/body/) antes del contenido del encabezado/pie de página. |
| [set_PrintColBlack](./set_printcolblack/)(bool) | Imprimir colores en blanco y negro sin tramado. |
| [set_SelectFldWithFirstOrLastChar](./set_selectfldwithfirstorlastchar/)(bool) | Seleccionar campo cuando se selecciona el primer o último carácter. |
| [set_ShapeLayoutLikeWW8](./set_shapelayoutlikeww8/)(bool) | Emular el ajuste de texto de Word 97 alrededor de objetos flotantes. |
| [set_ShowBreaksInFrames](./set_showbreaksinframes/)(bool) | Mostrar saltos de página/columna presentes en los marcos. |
| [set_SpaceForUL](./set_spaceforul/)(bool) | Agregar espacio adicional debajo de la línea base para texto asiático oriental subrayado. |
| [set_SpacingInWholePoints](./set_spacinginwholepoints/)(bool) | Solo expandir/contraer texto por puntos completos. |
| [set_SplitPgBreakAndParaMark](./set_splitpgbreakandparamark/)(bool) | Siempre mover la marca de [Paragraph](../../aspose.words/paragraph/) a la página después de un salto de página. |
| [set_SubFontBySize](./set_subfontbysize/)(bool) | Incrementar la prioridad del tamaño de [Font](../../aspose.words/font/) durante la sustitución de [Font](../../aspose.words/font/). |
| [set_SuppressBottomSpacing](./set_suppressbottomspacing/)(bool) | Ignorar la altura exacta de línea para la última línea en la página. |
| [set_SuppressSpacingAtTopOfPage](./set_suppressspacingattopofpage/)(bool) | Ignorar la altura mínima de línea para la primera línea en la página. |
| [set_SuppressSpBfAfterPgBrk](./set_suppressspbfafterpgbrk/)(bool) | No usar espacio antes en la primera línea después de un salto de página. |
| [set_SuppressTopSpacing](./set_suppresstopspacing/)(bool) | Ignorar la altura mínima y exacta de línea para la primera línea en la página. |
| [set_SuppressTopSpacingWP](./set_suppresstopspacingwp/)(bool) | Emular el interlineado de WordPerfect 5.x. |
| [set_SwapBordersFacingPgs](./set_swapbordersfacingpgs/)(bool) | Intercambiar los bordes de [Paragraph](../../aspose.words/paragraph/) en páginas impares. |
| [set_SwapInsideAndOutsideForMirrorIndentsAndRelativePositioning](./set_swapinsideandoutsideformirrorindentsandrelativepositioning/)(bool) | Especifica intercambiar interior y exterior para sangrías espejo y posicionamiento relativo. |
| [set_TransparentMetafiles](./set_transparentmetafiles/)(bool) | Especifica no dejar en blanco el área detrás de imágenes metafile. |
| [set_TruncateFontHeightsLikeWP6](./set_truncatefontheightslikewp6/)(bool) | Emular el cálculo de altura de [Font](../../aspose.words/font/) en WordPerfect 6.x. |
| [set_UICompat97To2003](./set_uicompat97to2003/)(bool) | Verdadero para desactivar la funcionalidad de la UI que no es compatible con Word97-2003. El valor predeterminado es **false**. |
| [set_UlTrailSpace](./set_ultrailspace/)(bool) | Subrayar todos los espacios finales. |
| [set_UnderlineTabInNumList](./set_underlinetabinnumlist/)(bool) | Subrayar el carácter siguiente después de la numeración. |
| [set_UseAltKinsokuLineBreakRules](./set_usealtkinsokulinebreakrules/)(bool) | Usar conjunto alternativo de reglas de salto de línea para asiático oriental. |
| [set_UseAnsiKerningPairs](./set_useansikerningpairs/)(bool) | Usar pares de kerning ANSI de [Fonts](../../aspose.words.fonts/). |
| [set_UseFELayout](./set_usefelayout/)(bool) | No omitir el código de [Layout](../../aspose.words.layout/) para asiático oriental/escritura compleja. |
| [set_UseNormalStyleForList](./set_usenormalstyleforlist/)(bool) | No aplicar automáticamente la [Paragraph](../../aspose.words/paragraph/)[Style](../../aspose.words/style/) de lista al texto con viñetas/numerado. |
| [set_UsePrinterMetrics](./set_useprintermetrics/)(bool) | Usar métricas de impresora para mostrar documentos. |
| [set_UseSingleBorderforContiguousCells](./set_usesingleborderforcontiguouscells/)(bool) | Usar reglas simplificadas para conflictos de [Border](../../aspose.words/border/) de tabla. |
| [set_UseWord2002TableStyleRules](./set_useword2002tablestylerules/)(bool) | Emular las reglas de [Style](../../aspose.words/style/) de tabla de Word 2002. |
| [set_UseWord2010TableStyleRules](./set_useword2010tablestylerules/)(bool) | Especifica usar reglas de estilo de tabla de Word2010. |
| [set_UseWord97LineBreakRules](./set_useword97linebreakrules/)(bool) | Emular el salto de línea de asiático oriental de Word 97. |
| [set_WPJustification](./set_wpjustification/)(bool) | Emular WordPerfect 6.x [Paragraph](../../aspose.words/paragraph/) Justificación. |
| [set_WPSpaceWidth](./set_wpspacewidth/)(bool) | Especifica si se debe establecer el ancho de un espacio como se hace en WordPerfect 5.x. |
| [set_WrapTrailSpaces](./set_wraptrailspaces/)(bool) | Ajuste de línea de espacios finales. |
| static [Type](./type/)() |  |

## Ejemplos



Muestra cómo establecer una especificación de cumplimiento OOXML a la que debe adherirse un documento guardado.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Si configuramos las opciones de compatibilidad para cumplir con Microsoft Word 2003,
// insertar una imagen definirá su forma usando VML.
doc->get_CompatibilityOptions()->OptimizeFor(Aspose::Words::Settings::MsWordVersion::Word2003);
builder->InsertImage(get_ImageDir() + u"Transparent background logo.png");

ASSERT_EQ(Aspose::Words::Drawing::ShapeMarkupLanguage::Vml, (System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_MarkupLanguage());

// El estándar OOXML "ISO/IEC 29500:2008" no admite formas VML.
// Si establecemos la propiedad "Compliance" del objeto SaveOptions a "OoxmlCompliance.Iso29500_2008_Strict",
// cualquier documento que guardemos pasando este objeto tendrá que seguir ese estándar.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>();
saveOptions->set_Compliance(Aspose::Words::Saving::OoxmlCompliance::Iso29500_2008_Strict);
saveOptions->set_SaveFormat(Aspose::Words::SaveFormat::Docx);

doc->Save(get_ArtifactsDir() + u"OoxmlSaveOptions.Iso29500Strict.docx", saveOptions);

// Nuestro documento guardado define la forma usando DML para adherirse al estándar OOXML "ISO/IEC 29500:2008".
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OoxmlSaveOptions.Iso29500Strict.docx");

ASSERT_EQ(Aspose::Words::Drawing::ShapeMarkupLanguage::Dml, (System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_MarkupLanguage());
```


Muestra cómo alinear verticalmente el contenido de texto de un cuadro de texto.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 200, 200);

// Establezca la propiedad "VerticalAnchor" a "TextBoxAnchor.Top" para
// alinear el texto en este cuadro de texto con el lado superior de la forma.
// Establezca la propiedad "VerticalAnchor" a "TextBoxAnchor.Middle" para
// alinear el texto en este cuadro de texto al centro de la forma.
// Establezca la propiedad "VerticalAnchor" a "TextBoxAnchor.Bottom" para
// alinear el texto en este cuadro de texto a la parte inferior de la forma.
shape->get_TextBox()->set_VerticalAnchor(verticalAnchor);

builder->MoveTo(shape->get_FirstParagraph());
builder->Write(u"Hello world!");

// La alineación vertical del texto dentro de los cuadros de texto está disponible a partir de Microsoft Word 2007.
doc->get_CompatibilityOptions()->OptimizeFor(Aspose::Words::Settings::MsWordVersion::Word2007);
doc->Save(get_ArtifactsDir() + u"Shape.VerticalAnchor.docx");
```

## Ver también

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
