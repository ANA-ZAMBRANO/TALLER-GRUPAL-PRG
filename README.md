# TALLER-GRUPAL-PRG
--CONSTRUCTORES--
TALLER GRUPAL
ste código desarrolla una aplicación de escritorio en Java que permite a los usuarios visualizar datos sobre los constructores de Fórmula 1 en un año específico, utilizando una interfaz gráfica de usuario (GUI). La información se obtiene de una base de datos PostgreSQL y se muestra en una tabla interactiva.
Descripción General del Código
1.	Conexión a la Base de Datos:
o	El código establece una conexión con una base de datos PostgreSQL específica (Formula1) usando DriverManager.getConnection.
2.	Interfaz Gráfica de Usuario (GUI):
o	Se crea una ventana (JFrame) titulada "Tabla de Constructores por Año".
o	En la parte superior de la ventana, se coloca un menú desplegable (JComboBox) que permite seleccionar un año.
o	En el centro de la ventana, se muestra una tabla (JTable) que contiene datos sobre los constructores de Fórmula 1.
3.	Poblar el Menú Desplegable:
o	El menú desplegable se llena con los años disponibles obtenidos de la base de datos mediante una consulta SQL.
4.	Actualización de la Tabla:
o	Al seleccionar un año en el menú desplegable, se ejecuta una tarea en segundo plano (utilizando SwingWorker) para consultar la base de datos y obtener información sobre los constructores de ese año.
o	Los datos obtenidos incluyen el nombre del constructor, el número de victorias, los puntos totales y el ranking.
o	Estos datos se utilizan para actualizar el modelo de la tabla, lo que a su vez actualiza la visualización en la interfaz gráfica.
Detalles de Implementación
•	connectDB(): Método para establecer la conexión con la base de datos PostgreSQL.
•	createGUI(): Método que configura y muestra la interfaz gráfica inicial.
•	populateComboBox(): Método que llena el JComboBox con los años disponibles desde la base de datos.
•	updateTableInBackground(): Método que realiza una consulta en segundo plano para actualizar los datos de la JTable basándose en el año seleccionado.
Componentes de la GUI
1.	JFrame: La ventana principal de la aplicación.
2.	JComboBox: Menú desplegable que permite seleccionar un año.
3.	JTable: Tabla que muestra la información de los constructores.
4.	DefaultTableModel: Modelo de datos para la tabla.
5.	JScrollPane: Contenedor que permite desplazarse por la tabla.
Flujo de Trabajo
1.	Inicio de la Aplicación:
o	La aplicación se inicia mediante el método main, que llama a SwingUtilities.invokeLater para asegurar que la creación de la GUI se realice en el hilo de eventos de Swing.
2.	Selección del Año:
o	Al seleccionar un año en el JComboBox, se desencadena un evento que llama a updateTableInBackground.
3.	Consulta y Actualización:
o	updateTableInBackground ejecuta una consulta SQL en segundo plano para obtener datos de constructores.
o	Los datos obtenidos se procesan y se actualiza el DefaultTableModel de la JTable, refrescando la vista en la GUI.
Propósito
El propósito de este código es proporcionar una herramienta visual e interactiva para consultar y visualizar datos históricos sobre los constructores de Fórmula 1, permitiendo al usuario seleccionar diferentes años y ver los datos correspondientes de manera rápida y sencilla.

![image](https://github.com/ANA-ZAMBRANO/TALLER-GRUPAL-PRG/assets/169195758/ebc738b7-a8ca-4190-bec6-bc79c952c297)
![image](https://github.com/ANA-ZAMBRANO/TALLER-GRUPAL-PRG/assets/169195758/d31441ba-0679-4cec-b446-3c8c1f88153a)



