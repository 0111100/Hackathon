### Team: CyberDrivers
# Informe de Auditoría de Seguridad

## Resumen Ejecutivo

La presente auditoría de seguridad ha sido realizada con el objetivo de identificar vulnerabilidades en el sistema de Ubuntu y proporcionar recomendaciones para mejorar su seguridad. En este informe se detallarán las vulnerabilidades encontradas, su ubicación, cómo fueron descubiertas, potencial impacto dentro del sistema, pruebas de concepto (PoC) de explotación y recomendaciones para mitigar los riesgos identificados.

## Vulnerabilidades Detectadas

1. **Acceso al Modo de Recuperación de Ubuntu para Obtener Acceso Root**

## Detalles de las Vulnerabilidades

### 1. Acceso al Modo de Recuperación de Ubuntu para Obtener Acceso Root

**Descripción:**
La vulnerabilidad consiste en la posibilidad de acceder al modo de recuperación de Ubuntu, lo que permite obtener acceso root al sistema, lo cual representa un riesgo significativo para la seguridad.

**Ubicación:**
El modo de recuperación de Ubuntu se encuentra en el proceso de arranque del sistema y puede ser accedido durante el inicio del sistema operativo.

**Cómo se Descubrió:**
La vulnerabilidad fue descubierta durante el análisis del proceso de arranque del sistema operativo Ubuntu.

**Cómo se Exploita - PoC:**
1. Reiniciar el sistema y durante el inicio presionar la tecla `Esc` o `Shift` para acceder al menú de arranque.
2. Seleccionar la opción "Modo de recuperación" o "Recovery Mode".
3. Acceder al shell de root sin necesidad de autenticación.

**Potencial Impacto dentro del Sistema - CVSS:**
- CVSS Base Score: 9.8 (Crítico)
- Vector de Acceso: Local
- Complejidad de Acceso: Baja
- Autenticación: No se requiere
- Impacto en la Confidencialidad: Alto
- Impacto en la Integridad: Alto
- Impacto en la Disponibilidad: Alto

**Recomendaciones:**
- Configurar el gestor de arranque para requerir autenticación antes de acceder al modo de recuperación.
- Implementar medidas de seguridad adicionales para proteger el acceso al modo de recuperación, como el cifrado del disco o la configuración del BIOS/UEFI.
- Monitorizar y registrar los intentos de acceso al modo de recuperación para detectar posibles intentos de intrusión.

## Contraseñas Encriptadas y Desencriptadas

### Contraseña 1:

**Encriptada (Base64):**
```
RkxBR3s5OTRkMDZmNzE5YmI4ZGY0YjI5OTMyOWI5OGI5YWVkYX0K
```

**Desencriptada:**
```
FLAG{994d06f719bb8df4b299329b98b9aeda}
```

### Contraseña 2:

**Encriptada (Base64):**
```
RkxBR3sxMGV1NDM3YTI3NWNmZjFjMDNkZWQ5OGYyMjUyYjZhNX0K
```

**Desencriptada:**
```
FLAG{10eu437a275cff1c03ded98f2252b6a5}
```

**Explicación de Desencriptación:**
Para desencriptar las contraseñas en base64, se utilizó un decodificador de base64. La cadena de texto en base64 se convierte en una secuencia de bytes que luego se interpreta como texto plano. Este proceso es reversible y permite obtener la contraseña original a partir de la versión encriptada en base64.

## Recursos Utilizados

Durante la auditoría, se utilizaron diversos recursos externos y técnicas de análisis de seguridad para identificar y evaluar las vulnerabilidades del sistema.

## Conclusiones

En base a las vulnerabilidades identificadas y las recomendaciones proporcionadas, se recomienda tomar medidas inmediatas para mitigar los riesgos de seguridad y fortalecer la protección del sistema de Ubuntu.
