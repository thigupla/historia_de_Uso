# historia_de_Uso
l Diagrama de Casos de Uso (Mermaid Syntax)

El siguiente bloque de código es el que genera la imagen visualizada. No modifiques las líneas que contienen las tres comillas invertidas (```) ni la palabra `mermaid`.

%% Use Case Diagram (Diagrama de Casos de Uso)
graph TD
    %% Define los actores
    actor("Administrador") as A
    actor("Empleado de Almacen") as E
    actor("Jefe de Compras") as J

    %% Define los Casos de Uso (RFs)
    subgraph Sistema de Inventario
        CU1[Gestionar Productos (RF02)]
        CU2[Registrar Pedido (RF03)]
        CU3[Actualizar Estado de Pedido (RF04)]
        CU4[Recibir Notificación de Stock Bajo (RF05)]
        CU5[Generar Reportes Básicos (F.05)]
        CU6[Gestionar Roles y Usuarios (F.03)]
    end

    %% Define las relaciones de los Actores (Quién hace qué)
    A --> CU1
    A --> CU6
    A --> CU5
    
    E --> CU1
    E --> CU2
    E --> CU3
    E --> CU5

    J --> CU4
    J --> CU5
