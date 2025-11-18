# Reporte de Auditoría

A continuación, se precisan las diferentes fallas en la aplicación. Del lado izquierdo tenemos el error y al lado derecho la posible corrección de mantenimiento. La solución es opcional, pero se debe aumentar la calidad del código para la siguiente auditoría.

## Reporte de auditoría proyecto sin refactorizar
<img width="592" height="246" alt="image" src="https://github.com/user-attachments/assets/eecad578-8159-4ce6-9601-971116b3f1f7" />

Los 36 problemas visibles se presentan varias veces a través del código y se dividen entre los siguientes:

### 1. Cambio en la definición de variables
Gran parte de los cambios que se deben hacer se enfocan en el manejo de variables. Es recomendable el uso de `let` para definir variables. Es importante revisar todo el módulo para hacer todas las correcciones correspondientes.
<img width="591" height="353" alt="image" src="https://github.com/user-attachments/assets/51ec91e6-144e-46ea-aac2-3bf49c0d9936" />

### 2. Prefiera `Number.parseInt` a `parseInt`
La idea es cambiar el uso de métodos. Se debe hacer el cambio de `parseInt` por `Number.parseInt()` haciendo el llamado a la clase `Number`.

<img width="589" height="239" alt="image" src="https://github.com/user-attachments/assets/1a052ada-f4f9-4d78-bc90-a2708c0d9e8a" />

### 3. Prefiera `Number.isNaN` a `isNaN`
Se recomienda priorizar los métodos y propiedades estáticos numéricos sobre sus equivalentes globales.
<img width="592" height="252" alt="image" src="https://github.com/user-attachments/assets/6277175e-f780-4e10-bdbe-cb63eba04a79" />

### 4. Se esperaba un bucle `for-of` en lugar de un bucle `for`
El uso de `for` a secas hace menos visible el código; se recomienda usar un `for-of`.
<img width="697" height="120" alt="image" src="https://github.com/user-attachments/assets/ee222a40-3407-4ba1-9fe5-6a7c941359c9" />
<img width="694" height="200" alt="image" src="https://github.com/user-attachments/assets/9f2325d4-d764-430c-85b8-ea60c13ee1ab" />

### 5. Refactoriza el código para evitar el uso de este literal booleano
<img width="694" height="351" alt="image" src="https://github.com/user-attachments/assets/df349e08-1ea4-44c0-8561-5921c73e9b48" />

### 6. El texto no cumple con el requisito mínimo de contraste con su fondo
<img width="695" height="274" alt="image" src="https://github.com/user-attachments/assets/9e1ceffa-355a-4e40-b05e-53c64a7a29cd" />

## Métricas del proyecto

| Métrica                    | Antes del refactor      | Después del refactor | Cambio |
|---------------------------|--------------------------|------------------------|--------|
| Seguridad (issues)        | 0                        | 0                      | Sin cambios |
| Fiabilidad (issues)       | 5                        | 5                      | Sin cambios |
| Mantenibilidad (issues)   | 36                       | 12                     | Mejora significativa (-24 issues) |
| Duplicaciones             | 0% (en 354 líneas)       | 0% (en 380 líneas)     | Sin cambios (más líneas, sigue en 0%) |
| Cobertura                 | Sin configurar           | Sin configurar         | Sin cambios |
| Temas aceptados           | 0                        | 0                      | Sin cambios |
| Puntos críticos seguridad | 0                        | 0                      | Sin cambios |
