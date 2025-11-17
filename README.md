graph TD
    %% Configuración del Diagrama
    direction LR

    %% 1. Definición de Actores
    A[Administrador]
    E[Empleado de Almacén]
    J[Jefe de Compras]

    %% 2. Definición del Sistema (Límite del Sistema)
    subgraph Sistema de Inventario
        CU1(Gestionar Productos - RF02)
        CU2(Registrar Pedido - RF03)
        CU3(Actualizar Estado de Pedido - RF04)
        CU4(Recibir Notificación de Stock Bajo - RF05)
        CU5(Generar Reportes - F.05)
        CU6(Gestionar Roles y Usuarios - F.03)
    end

    %% 3. Definición de las Relaciones (Interacciones)
    
    %% Relaciones del Administrador (A)
    A --> CU1
    A --> CU6
    A --> CU5

    %% Relaciones del Empleado de Almacén (E)
    E --> CU1
    E --> CU2
    E --> CU3
    E --> CU5

    %% Relaciones del Jefe de Compras (J)
    J --> CU4
    J --> CU5

