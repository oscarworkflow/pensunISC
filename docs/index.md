<html>
<head>
    <meta charset="utf-8">
    <meta http-equiv="Content-Type" content="text/html; charset=utf-8">
    <title>jsMind</title>
    <link type="text/css" rel="stylesheet" href="style/jsmind.css" />
    <style type="text/css">
        #jsmind_container{
            width:100%;
            height:1700px;
            border:solid 1px #ccc;
            /*background:#f4f4f4;*/
            background:#f4f4f4;
        }
        .container-lg { max-width: 100% !important; }
    </style>
</head>
<body>
<div id="jsmind_container"></div>
<script type="text/javascript" src="js/jsmind.js"></script>
<script type="text/javascript" src="js/jsminddraggable.js"></script>
<script type="text/javascript">
    function load_jsmind(){
        var mind = {
            "meta":{
                "name":"demo",
                "author":"hizzgdev@163.com",
                "version":"0.2",
            },
            "format":"node_array",
            "data":[
                {"id":"root", "isroot":true, "topic":"INGENIERIA DE SISTEMAS DE COMPUTACION"},

                {"id":"1", "parentid":"root", "topic":"CUATRIMESTRE: 1", "background-color":"#0ff0ff"},
                {"id":"ESP101", "parentid":"1", "topic":"ESP101 - ANALISIS DE TEXTOS DISCURSIVOS"},
                {"id":"INF319", "parentid":"1", "topic":"INF319 - COMPUTACION I"},
                {"id":"MAT126", "parentid":"1", "topic":"MAT126 - MATEMATICA BASICA PARA INGENIERIA"},
                {"id":"SOC011", "parentid":"1", "topic":"SOC011 - HISTORIA SOCIAL DOMINICANA"},
                {"id":"SOC030", "parentid":"1", "topic":"SOC030 - ORIENTACION UNIVERSITARIA"},
                {"id":"SOC043", "parentid":"1", "topic":"SOC043 - GESTION AMBIENTAL"},
                {"id":"ENG001", "parentid":"1", "topic":"ENG001 - INGLES I"},

                //{"id":"2", "parentid":"1", "topic":"CUATRIMESTRE: 2", "background-color":"#0ff0ff"},
                {"id":"ESP102", "parentid":"ESP101", "topic":"ESP102 - REDACCION DE TEXTOS DISCURSIVOS I"},
                {"id":"INF321", "parentid":"INF319", "topic":"INF321 - ALGORITMOS"},
                {"id":"MAT127", "parentid":"MAT126", "topic":"MAT127 - MATEMATICA SUPERIOR PARA INGENIERIA	"},
                {"id":"TEC111", "parentid":"MAT126", "topic":"TEC111 - FISICA GENERAL"},
                {"id":"TEC132", "parentid":"MAT126", "topic":"TEC132 - LABORATORIO FISICA GENERAL"},
                {"id":"ENG002", "parentid":"ENG001", "topic":"ENG002 - INGLES II"},


                {"id":"3", "parentid":"root", "topic":"CUATRIMESTRE: 3", "background-color":"#0ff0ff", "direction":"left"},
                {"id":"ESP103", "parentid":"ESP102", "topic":"ESP103 - REDACCION DE TEXTOS DISCURSIVOS II"},
                {"id":"INF140", "parentid":"INF321", "topic":"INF140 - PROGRAMACION ESTRUCTURADA"},
                {"id":"INF323", "parentid":"INF321", "topic":"INF323 - ARQUITECTURA DEL COMPUTADOR	"},
                {"id":"MAT222", "parentid":"MAT127", "topic":"MAT222 - ALGEBRA LINEAL"},
                {"id":"SOC031", "parentid":"3", "topic":"SOC031 - ETICA PROFESIONAL"},
                {"id":"SOC150", "parentid":"3", "topic":"SOC150 - RELACIONES HUMANAS"},
                {"id":"ENG003", "parentid":"ENG002", "topic":"ENG003 - INGLES III"},

                //{"id":"4", "parentid": "root", "topic":"CUATRIMESTRE: 4", "background-color":"#0ff0ff"},
                {"id":"CON107", "parentid": "MAT222, SOC031", "topic":"CON107 - CONTABILIDAD EMPRESARIAL"},
                {"id":"INF111", "parentid": "INF140", "topic":"INF111 - PROGRAMACION ORIENTADA A OBJETOS"},
                {"id":"INF160", "parentid": "INF140", "topic":"INF160 - ANALISIS Y DISEÑO DE SISTEMAS I"},
                {"id":"INF168", "parentid": "INF323", "topic":"INF168 - SISTEMAS OPERATIVOS I"},
                {"id":"MAT131", "parentid": "MAT222", "topic":"MAT131 - CALCULO Y GEOMETRIA ANALITICA I"},
                {"id":"ENG004", "parentid": "ENG003", "topic":"ENG004 - INGLES IV"},

                {"id":"INF152", "parentid": "INF111", "topic":"INF152 - ESTRUCTURA DE DATOS"},
                {"id":"INF161", "parentid": "INF160", "topic":"INF161 - ANALISIS Y DISEÑO DE SISTEMAS II"},
                {"id":"MAT132", "parentid": "MAT131", "topic":"MAT132 - CALCULO Y GEOMETRIA ANALITICA II"},
                {"id":"TEC113", "parentid": "TEC132", "topic":"TEC113 - FISICA ELECTRICA", "background-color":"red"},
                {"id":"TEC120", "parentid": "TEC132", "topic":"TEC120 - LABORATORIO FISICA ELECTRICA"},
                {"id":"ENG005", "parentid": "ENG004", "topic":"ENG005 - INGLES V"},

                {"id":"INF166", "parentid": "INF168", "topic":"INF166 - TELEPROCESO I"},
                {"id":"INF169", "parentid": "INF168", "topic":"INF169 - SISTEMAS OPERATIVOS II"},
                {"id":"MAT151", "parentid": "MAT132", "topic":"MAT151 - MATEMATICA DISCRETA", "background-color":"red"},
                {"id":"MAT252", "parentid": "MAT132", "topic":"MAT252 - PROBABILIDAD Y ESTADISTICA"},
                {"id":"TEC123", "parentid": "TEC120", "topic":"TEC123 - LABOR.CIRCUITOS ELECTRICOS I", "background-color":"red"},
                {"id":"TEC146", "parentid": "TEC120", "topic":"TEC146 - CIRCUITOS ELECTRICOS I", "background-color":"red"},
                {"id":"ENG006", "parentid": "ENG005", "topic":"ENG006 - INGLES VI", "background-color":"red"},

                {"id":"7", "parentid": "root", "topic":"CUATRIMESTRE: 7", "background-color":"#0ff0ff", "direction":"left"},
                {"id":"ADM091", "parentid": "7", "topic":"ADM091 - ADMINISTRACION I"},
                {"id":"INF167", "parentid": "INF166", "topic":"INF167 - TELEPROCESO II"},
                {"id":"INF315", "parentid": "INF169", "topic":"INF315 - SISTEMAS OPERATIVOS III"},
                {"id":"INF402", "parentid": "MAT151", "topic":"INF402 - FUNDAMENTOS DE BASES DE DATOS", "background-color":"red"},
                {"id":"SOC250", "parentid": "7", "topic":"SOC250 - METODOLOGIA DE LA INVESTIGACION CIENTIFICA"},
                {"id":"ENG007", "parentid": "ENG006", "topic":"ENG007 - INGLES VII", "background-color":"red"},

                {"id":"ADM150", "parentid": "ADM091", "topic":"ADM150 - GERENCIA DE PROCESOS"},
                {"id":"INF309", "parentid": "INF315", "topic":"INF309 - TECNOLOGIAS DE INTERNET"},
                {"id":"INF325", "parentid": "INF152", "topic":"INF325 - PROGRAMACION VISUAL"},
                {"id":"INF327", "parentid": "INF169", "topic":"INF327 - COMUNICACIONES"},
                {"id":"TEC148", "parentid": "TEC146", "topic":"TEC148 - ELECTRONICA I", "background-color":"red"},
                {"id":"TEC155", "parentid": "TEC146", "topic":"TEC155 - LAB.DE ELECTRONICA I", "background-color":"red"},
                {"id":"ENG008", "parentid": "ENG007", "topic":"ENG008 - INGLES VIII", "background-color":"red"},

                {"id":"IDI045", "parentid": "ENG008", "topic":"IDI045 - INGLES PARA INFORMATICA I", "background-color":"red"},
                {"id":"IND371", "parentid": "MAT252", "topic":"IND371 - INVESTIGACION DE OPERACIONES PARA INFORMATICA"},
                {"id":"INF307", "parentid": "INF327", "topic":"INF307 - ADMINISTRACION DE REDES"},
                {"id":"INF324", "parentid": "INF309", "topic":"INF324 - INTROD. INTELIGENCIA ARTIF."},
                {"id":"INF403", "parentid": "INF325", "topic":"INF403 - BASES DE DATOS DISTRIBUIDAS Y MULTIDIMENSIONALES"},
                {"id":"TEC190", "parentid": "TEC155", "topic":"TEC190 - LOGICA DIGITAL I", "background-color":"red"},
                {"id":"TEC200", "parentid": "TEC155", "topic":"TEC200 - LAB. LOGICA DIGITAL I", "background-color":"red"},

                {"id":"10", "parentid": "root", "topic":"CUATRIMESTRE: 10", "background-color":"#0ff0ff", "direction":"left"},
                {"id":"DER179", "parentid": "10", "topic":"DER179 - DERECHO APLICADO A LA INFORMATICA"},
                {"id":"IDI046", "parentid": "IDI045", "topic":"IDI046 - INGLES PARA INFORMATICA II", "background-color":"red"},
                {"id":"IND423", "parentid": "IND371", "topic":"IND423 - INGENIERIA ECONOMICA", "background-color":"red"},
                {"id":"INF329", "parentid": "INF307", "topic":"INF329 - SEGURIDAD"},
                {"id":"ISC404", "parentid": "TEC190", "topic":"ISC404 - ESTANDARES Y TENDENCIAS DE LA INDUSTRIA", "background-color":"red"},
                {"id":"TEC614", "parentid": "INF324", "topic":"TEC614 - AUTOMATIZACION Y ROBOTICA", "background-color":"red", "direction":"left"},
                {"id":"11", "parentid": "root", "topic":"CUATRIMESTRE: 11", "background-color":"#0ff0ff", "direction":"left"},
                {"id":"ADM120", "parentid": "ADM150", "topic":"ADM120 - LIDERAZGO Y TECNICAS DE SUPERVISION"},
                {"id":"ADM535", "parentid": "ADM150", "topic":"ADM535 - ACTITUD EMPRENDEDORA"},
                {"id":"INF204", "parentid": "INF329", "topic":"INF204 - ADMINISTRACION DE CENTROS"},
                {"id":"INF328", "parentid": "INF324", "topic":"INF328 - SISTEMAS BASADOS EN EL CONOCIMIENTO"},
                {"id":"INF407", "parentid": "INF329", "topic":"INF407 - HACKING ETICO"},
                {"id":"ISC406", "parentid": "INF329", "topic":"ISC406 - COMPUTACION FORENSE", "background-color":"red"},
                {"id":"SOC281", "parentid": "11", "topic":"SOC281 - SEMINARIO DE GRADO", "background-color":"red"},


            ]
        };
        var options = {
            container:'jsmind_container',
            editable:true,
            theme:'primary'
        }
        var jm = jsMind.show(options,mind);
        // jm.set_readonly(true);
        // var mind_data = jm.get_data();
        // alert(mind_data);
        jm.add_node("sub2","sub23", "new node", {"background-color":"red"});
        jm.set_node_color('sub21', 'green', '#ccc');
    }

    load_jsmind();
</script>
</body>
</html>
