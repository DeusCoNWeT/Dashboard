# Explicación de esta rama

Para ver como funciona esto vaya al readme de otro branch por favor.
Esto es solo una explicacion de esta rama.


**"funciones" añadidas:**
  - supr+mayusc --> eliminar componente
  - enter en el ultimo recuadro de conexion para añadir conexión
  - tratamiento de errores (alert de por qué no puedes hacer la conexión y cosas así, no mucho más)
  
## Componentes añadidos (bower.json)
Mapa que muestra el tráfico. Hay dos versiones, la normal y la "pro".
      
  - Normal --> introduces la ciudad en el componente de tráfico y al darle a enter te muestra las incidencias en el mapa.      Errores conocidos:
      -si el array de trafico es muy largo en el dashboard no se pasa entero y da error (en polymer serve-o se pasa entero)
      
  - Pro --> te mueves por el mapa, le das a buscar aquí (o algo así se llama el botón), y te muestra tanto en el 
            mapa como en el componente de tráfico los incidentes. Errores conocidos
                -En ciudades ambiguas (que haya varias llamadas igual no sabes cuál te va a dar). Lo puedo arreglar creo,
                      pasa mucho en EEUU
                -Al pinchar en carreteras te puede dar incidente en cualquier punto de la carretera
                -si el array de trafico es muy largo en el dashboard no se pasa entero y da error (en polymer serve-o se pasa entero)
                
                
  ### Para conectar las versiones:
  - Versión básica:
    - radio de traffic-incidents --> radio de map-component
    - lat de traffic-incidents --> latitude de map-component
    - long de traffic-incidents --> longitude de map-component
    - traffic-info2 de traffic-incidents --> traffic-info de map-component

  - version "pro"
    - traffic-info2 de traffic-incidents --> traffic-info de map-component
    - radio de traffic-incidents --> radio de map-component
    - city de map-component --> city detraffic-incidents
    
### Componentes  
- El componente de trafico:
  - Version básica: se encuentra en **"traffic-incidents": "Rafata/trafficMortega#tpolymer2"**  o en  **"traffic-incidents": "Rafata8/mapaTrafico#*"** . El primero está en polymer 2, el segundo está en Polymer 1
  - Versión pro: "traffic-incidents": "Rafata8/mapaTrafico#*". Se podría usar también los dos de la báica, pero quedan peor para esta parte
- El componente de mapa:
  - Versión básica: **"map-component": "Rafata8/mapaTrafico#*"**
  - Versión pro: **"map-component": "Rafata8/mapaTrafico#pro"**
                

