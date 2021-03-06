# <a name="consolidated-sales-report-task-pane-add-in-sample-for-excel-2016"></a>Ejemplo de complemento del panel de tareas de informe de ventas consolidadas para Excel 2016

_Se aplica a: Excel 2016_

Este complemento del panel de tareas muestra cómo consolidar datos de varias hojas de cálculo mediante las API de JavaScript de Excel 2016. Hay dos tipos: editor de código y Visual Studio.

![Ejemplo de informe de ventas consolidadas](../images/ConsolidatedSalesReport_report.PNG)

## <a name="try-it-out"></a>Pruébelo
### <a name="code-editor-version"></a>Versión del editor de código

La forma más sencilla de implementar y probar el complemento consiste en copiar los archivos en un recurso compartido de red.

1.  Hospede los archivos en el proyecto del Editor de código mediante su servidor favorito.
2.  Edite los elementos \<SourceLocation\> y \<Url\> del archivo de manifiesto (ConsolidatedSaleReportManifest.xml) para que apunte a la ubicación hospedada del paso 1 (por ejemplo, https://hostlocal/informedeventasconsolidadas/home.html).
3.  Copie el manifiesto (ConsolidatedSalesReportManifest.xml) en un recurso compartido de red (por ejemplo, \\\MiRecursoCompartido\\MisManifiestos).
4.  Agregue la ubicación del recurso compartido que contiene el manifiesto como un catálogo de aplicaciones de confianza en Excel.

    a.  Inicie Excel y abra una hoja de cálculo en blanco.

    b.  Elija la pestaña **Archivo** y, a continuación, **Opciones**.

    c.  Elija **Centro de confianza** y, a continuación, el botón **Configuración del Centro de confianza**.

    d.  Elija **Catálogos de complementos de confianza**.

    e.  En el cuadro **URL del catálogo**, escriba la ruta de acceso al recurso compartido de red que creó en el paso 3 y, a continuación, elija **Agregar catálogo**.

   f. Active la casilla **Mostrar en el menú** y elija **Aceptar**. Aparecerá un mensaje para informarle de que la configuración se aplicará la próxima vez que inicie Office.

5.  Pruebe y ejecute el complemento.

    a.  En la pestaña **Insertar** de Excel 2016, elija **Mis complementos**.

    b.  En el cuadro de diálogo **Complementos de Office**, elija **Carpeta compartida**.

    c.  Elija **Ejemplo de informe de ventas consolidadas**>**Insertar**. El complemento se abrirá en un panel de tareas a la derecha de la hoja de cálculo actual, como se muestra en la ilustración siguiente.

   ![Ejemplo de informe de ventas consolidadas](../images/ConsolidatedSalesReport_taskpane.PNG)

    d.  Seleccione las casillas de América, Asia y Europa y haga clic en el botón **Consolidar**.  Esto creará una nueva hoja en el panel que mostrará un resumen de todas las hojas seleccionadas.

  ![Ejemplo de informe de ventas consolidadas](../images/ConsolidatedSalesReport_report.PNG)

### <a name="visual-studio-version"></a>Versión de Visual Studio
1.  Copie el proyecto en una carpeta local y abra Excel-Add-in-JS-ConsolidatedSalesReport.sln en Visual Studio.
2.  Pulse F5 para crear e implementar el complemento de ejemplo. Excel se inicia y se abre el complemento en un panel de tareas a la derecha de una hoja de cálculo en blanco, como se muestra en la siguiente ilustración.

   ![Ejemplo de informe de ventas consolidadas](../images/ConsolidatedSalesReport_taskpane.PNG)

    d.  Seleccione las casillas de América, Asia y Europa y haga clic en el botón **Consolidar**.  Esto creará una nueva hoja en el panel que mostrará un resumen de todas las hojas seleccionadas.

  ![Ejemplo de informe de ventas consolidadas](../images/ConsolidatedSalesReport_report.PNG)


### <a name="learn-more"></a>Obtener más información

1.  [Introducción a la programación de complementos de Excel](https://github.com/OfficeDev/office-js-docs/blob/master/excel/excel-add-ins-programming-overview.md)
2.  [Explorador de fragmentos de código para Excel](http://officesnippetexplorer.azurewebsites.net/#/snippets/excel)
3.  [Ejemplos de código de complementos de Excel](https://github.com/OfficeDev/office-js-docs/blob/master/excel/excel-add-ins-code-samples.md)
4.  [Referencia de la API de JavaScript de complementos de Excel](https://github.com/OfficeDev/office-js-docs/blob/master/excel/excel-add-ins-javascript-reference.md)
5.  [Compilar el primer complemento de Excel](https://github.com/OfficeDev/office-js-docs/blob/master/excel/build-your-first-excel-add-in.md)