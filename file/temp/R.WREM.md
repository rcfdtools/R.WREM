R.WREM
Duration: 5 weeks (W1-4h, W2-4h, W3-4h, W4-6h, W5-6h)

● 5 semana (viernes 10 de julio) 07:30-09:30  


HECRAS_Prototype1D_v0
HECRAS_Prototype2D_v0
HECRAS_River_v0
Bridge 2D https://www.youtube.com/watch?v=yBpWdOBdasU

Q 28m3/s en sifon Fa
ARF Q
0.23 7.7
0.5 159.4

ERA5
North 5.3
South 4.2
East -73.5
West -74.9

ERA5_land_monthly_climatological_var_010dd_ssr_uv10_CuencaRioBogota.nc
https://esa-landcover-cci.org/
https://esa-worldcover.org/en
Minus 273.15

Nivel hidrológico superficial
● N1-AH
● N2-ZH
● N3-SZH
● N4-Subcuencas aportantes al Río Bogotá


CNESource = if("Entidad" = 'INSTITUTO DE HIDROLOGÍA METEOROLOGÍA Y ESTUDIOS AMBIENTALES', 'CNE', 'CNE_OE')

Sample raster values

Distance between stations
	TIN Mesh Creation
	Export mesh faces
	Polygons to lines
	Explode lines
	D2D = length(@geometry)/1000
	D3D = length3D(@geometry)/1000
	Filter "D3D" <= 200

Filtros e interpolaciones IDW:
    "FilterZE" = 1 AND "n" >= 8 AND "tr" = 2.33 AND "pmax24hr" > 0
	"FilterZE" = 1 AND "n" >= 8 AND "tr" = 100 AND "pmax24hr" > 0  AND "pmax24hr" <= 1000
	Gumbel Tr 2.33 y 100 años, p:12, Cellsize:100
	BestFit Tr 2.33 y 100 años, p:12, Cellsize:100
	Demás distribuciones comunes usadas en hidrología con Tr 2.33 y 100.
	Con p=12 obtendrán la distribución espacial similar a los polígonos de Thiessen Voronio.

Filtro estaciones nivel de lámina

	"Categoria" IN ('Limnigráfica','Limnimétrica') AND "LYearSTW" >= 5 AND "Tecnologia" IN ('Automática con Telemetría','Automática con Telemetría, Convencional','Automática sin Telemetría')
	
	"Entidad" = 'EMPRESA DE ACUEDUCTO Y ALCANTARILLADO DE BOGOTA E.S.P' AND "Categoria" IN ('Limnigráfica','Limnimétrica') AND "Corriente" = 'BOGOTÁ'
	
	
Prompt: Duración promedio de la precipitación en la cuenca del Río Bogotá

	En la cuenca del río Bogotá, la precipitación no suele ser continua durante todo el día; se presenta principalmente a través de eventos intermitentes (chubascos o aguaceros). La duración promedio de estos eventos de lluvia oscila entre 1 y 4 horas, concentrándose fuertemente en las tardes y primeras horas de la noche.

	Factores climáticos y duración

	Régimen de lluvias: La cuenca presenta un régimen bimodal (dos temporadas de lluvias al año). La primera ocurre entre marzo y mayo, y la segunda entre octubre y mediados de diciembre.

	Acumulados mensuales: Durante los meses más lluviosos, como abril, la precipitación mensual puede llegar a 378 mm (en la ciudad de Bogotá). En total, el promedio anual de la ciudad es de 866 mm.

	Influencia orográfica: Los cerros orientales y la topografía condicionan la formación de las nubes y desencadenan tormentas que duran un par de horas, especialmente cuando hay humedad proveniente de los Llanos Orientales.

	Tiempo de concentración de la cuencaEn términos estrictamente hidrológicos, el tiempo de concentración (el tiempo que tarda una "gota de lluvia" desde la parte más lejana de la cuenca en llegar al cauce principal del río Bogotá) varía de forma considerable según la zona:

	Cuenca urbana y subcuencas: En microcuencas urbanas (como los ríos Torca, Salitre, Fucha o Tunjuelo), este tiempo puede ser muy rápido, de 1 a 3 horas tras iniciar un aguacero.

	Cuenca alta y media: El tiempo que tarda el agua en recorrer las partes más extensas puede oscilar entre 8 y 12 horas antes de que el caudal máximo alcance la cuenca baja.

Prompt (Google Chrome AI mode): Convert this chart in a day by day table
			

