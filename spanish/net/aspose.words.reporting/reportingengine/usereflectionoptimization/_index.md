---
title: ReportingEngine.UseReflectionOptimization
linktitle: UseReflectionOptimization
articleTitle: UseReflectionOptimization
second_title: Aspose.Words para .NET
description: Optimice las invocaciones de miembros de tipo personalizados con la propiedad UseReflectionOptimization de ReportingEngine. Mejore el rendimiento con la generación dinámica de clases para una mayor eficiencia.
type: docs
weight: 60
url: /es/net/aspose.words.reporting/reportingengine/usereflectionoptimization/
---
## ReportingEngine.UseReflectionOptimization property

Obtiene o establece un valor que indica si las invocaciones de miembros de tipo personalizado realizadas mediante la API de reflexión están optimizadas mediante la generación dinámica de clases. El valor predeterminado es`verdadero` .

```csharp
public static bool UseReflectionOptimization { get; set; }
```

## Observaciones

Hay algunos escenarios en los que es preferible deshabilitar esta optimización. Por ejemplo, si se trabaja constantemente con pequeñas colecciones de elementos de datos, la sobrecarga de la generación dinámica de clases puede ser más notable que la de las llamadas a la API de reflexión directa. Esta opción no tiene efecto cuando se ejecuta en iOS y no se utiliza la optimización de reflexión.

### Ver también

* class [ReportingEngine](../)
* espacio de nombres [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* asamblea [Aspose.Words](../../../)
