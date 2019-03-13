Para ver como funciona esto mejor vete a otra rama a verlo.
Esto es solo una explicacion de esta rama.

"funciones" añadidas:
  - supr+mayusc --> eliminar componente
  - enter en el ultimo recuadro de conexion para añadir conexión
  - tratamiento de errores (alert de por qué no puedes hacer la conexión y cosas así, no mucho más)
  
Mapa que muestra el tráfico. Hay dos versiones, la normal y la "pro".
      
  - Normal --> introduces la ciudad en el componente de tráfico y al darle a enter te muestra las incidencias en el mapa.      Errores conocidos:
      -si el array de trafico es muy largo en el dashboard no se pasa entero y da error (en polymer serve-o se pasa entero)
      
  - Pro --> te mueves por el mapa, le das a buscar aquí (o algo así se llama el botón), y te muestra tanto en el 
            mapa como en el componente de tráfico los incidentes. Errores conocidos
                -En ciudades ambiguas (que haya varias llamadas igual no sabes cuál te va a dar). Lo puedo arreglar creo,
                      pasa mucho en EEUU
                -Al pinchar en carreteras te puede dar incidente en cualquier punto de la carretera
                -si el array de trafico es muy largo en el dashboard no se pasa entero y da error (en polymer serve-o se pasa entero)
                
                
  Para conectar las versiones:
  para conectar la versión básica:
    radio de traffic-incidents --> radio de map-component
    lat de traffic-incidents --> latitude de map-component
    long de traffic-incidents --> longitude de map-component
    traffic-info2 de traffic-incidents --> traffic-info de map-component

para conectar la version "pro"
   traffic-info2 de traffic-incidents --> traffic-info de map-component
    radio de traffic-incidents --> radio de map-component
    city de map-component --> city de map-component traffic-incidents
    
 El componente de trafico se encuentra en Rafata/trafficMortega#tpolymer2  o en  "traffic-incidents": "Rafata8/mapaTrafico#*"
 
 el mapa se encuentra en "map-component": "Rafata8/mapaTrafico#*", el básico, y el pro en "map-component": "Rafata8/mapaTrafico#pro",
                

