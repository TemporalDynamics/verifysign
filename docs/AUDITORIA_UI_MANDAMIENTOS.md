# 🔍 AUDITORÍA UI/UX - Violaciones de los 20 Mandamientos

**Documento de trabajo para el desarrollador**

Este documento lista **TODAS las violaciones** encontradas en el código actual que rompen los 20 Mandamientos de EcoSign. Cada violación incluye:
- 📍 Ubicación exacta
- ❌ Texto/código actual
- ✅ Reemplazo correcto
- 🔢 Mandamiento violado

---

## 🎯 PRIORIDAD ALTA - Landing Page y UX Principal

### 1. LandingPageV2.jsx - Hero Section

**📍 Archivo:** `client/src/pages/LandingPageV2.jsx`

#### Violación #1: Promesas exageradas
**❌ ACTUAL:**
```jsx
"Tu trabajo merece una verdad que nadie pueda cuestionar"
```

**✅ REEMPLAZAR CON:**
```jsx
"Certificá tus documentos con evidencia verificable"
```

**🔢 Mandamiento:** XII - Nunca usar frases que suenen a promesas vacías

---

#### Violación #2: Tecnicismos en sección "Cómo funciona"
**❌ BUSCAR:** Cualquier mención de "hash", "blockchain", "timestamp", "SHA-256"

**✅ REEMPLAZAR:**
- "hash" → eliminar o usar "código único"
- "blockchain" → eliminar o usar "registro verificable"
- "timestamp" → "sellado de fecha y hora"
- "SHA-256" → eliminar completamente

**🔢 Mandamiento:** III - Nunca mostrar tecnicismos a usuarios finales

---

### 2. Dashboard.jsx - Header y mensajes

**📍 Archivo:** `client/src/pages/Dashboard.jsx`

#### Violación #3: Fondo azul en botones
**❌ BUSCAR:** Cualquier `bg-blue-500` o similar en contenedores grandes

**✅ REEMPLAZAR:**
```jsx
// De esto:
<div className="bg-blue-500 p-6 rounded-lg">
  <button>Certificar</button>
</div>

// A esto:
<div className="bg-white border border-soft p-6 rounded-lg">
  <button className="bg-accent hover:bg-accent-hover text-white">
    Certificar documento
  </button>
</div>
```

**🔢 Mandamiento:** XVIII - Nunca usar colores agresivos o saturados

---

#### Violación #4: Textos que sugieren "subir"
**❌ BUSCAR:** 
- "Subir documento"
- "Sube tu archivo"
- "Upload"

**✅ REEMPLAZAR:**
- "Certificar documento"
- "Elegí tu archivo"
- "Seleccioná tu documento"

**🔢 Mandamiento:** I - Nunca usar palabras que generen miedo o sospecha

---

### 3. CertificationFlow.jsx - Modal de certificación

**📍 Archivo:** `client/src/components/CertificationFlow.jsx`

#### Violación #5: Paso de "Sellar evidencia" con switches técnicos
**❌ BUSCAR:**
```jsx
// Paso con opciones de:
- Timestamp RFC 3161
- Anclaje en blockchain
- Capturar IP
```

**✅ ELIMINAR COMPLETAMENTE** este paso y sus opciones.

**✅ DEJAR SOLO 3 PASOS:**
1. Elegí tu archivo
2. Firmá
3. Listo

**🔢 Mandamiento:** IV - Nunca mezclar conceptos técnicos en el flujo de firma

---

#### Violación #6: Mensajes de progreso técnicos
**❌ BUSCAR:**
```jsx
"Generando hash SHA-256..."
"Calculando timestamp..."
"Anclando en blockchain..."
"Procesando firma criptográfica..."
```

**✅ REEMPLAZAR:**
```jsx
"Preparando tu certificado..."
"Ya casi está listo..."
"Finalizando..."
```

**🔢 Mandamiento:** XI - Nunca anunciar procesos internos

---

#### Violación #7: Cuadro azul de recomendación en firma legal
**❌ BUSCAR:**
```jsx
<div className="bg-blue-100 border border-blue-500 p-4">
  <p>⚠️ Se recomienda usar firma legal...</p>
</div>
```

**✅ REEMPLAZAR:**
```jsx
<div className="bg-bg-soft border-l-4 border-accent rounded-lg p-4">
  <h3 className="text-sm font-medium text-main mb-2">
    Firma legal (recomendada)
  </h3>
  <p className="text-xs text-muted">
    Usamos proveedores alineados con marcos como eIDAS, ESIGN y UETA para que la firma tenga validez legal internacional
  </p>
</div>
```

**🔢 Mandamiento:** XVIII - Nunca usar colores agresivos

---

### 4. VerifyPage.jsx - Verificación de documentos

**📍 Archivo:** `client/src/pages/VerifyPage.jsx`

#### Violación #8: Mostrar detalles técnicos de hash
**❌ BUSCAR:**
```jsx
"Hash SHA-256: abc123..."
"Timestamp RFC 3161: ..."
"Algoritmo: SHA-256"
```

**✅ ELIMINAR** todas las menciones técnicas.

**✅ MOSTRAR SOLO:**
```jsx
<div className="bg-accent-soft border-l-4 border-accent rounded-lg p-4">
  <CheckCircle className="w-5 h-5 text-accent" />
  <p className="text-sm font-medium text-main">Coincide</p>
  <p className="text-xs text-muted">
    Este documento es idéntico al que se certificó con este archivo .ECO
  </p>
</div>
```

**🔢 Mandamiento:** III - Nunca mostrar tecnicismos

---

#### Violación #9: Mensaje de error con "manipulación" o "falsificación"
**❌ BUSCAR:**
```jsx
"Posible manipulación del documento"
"Detectada falsificación"
"El archivo ha sido alterado fraudulentamente"
```

**✅ REEMPLAZAR:**
```jsx
<div className="bg-gray-50 border-l-4 border-gray-400 rounded-lg p-4">
  <AlertTriangle className="w-5 h-5 text-gray-600" />
  <p className="text-sm font-medium text-main">No coincide</p>
  <p className="text-xs text-muted">
    El documento no es igual al que se certificó con este archivo .ECO
  </p>
</div>
```

**🔢 Mandamiento:** VI - Nunca usar palabras que indiquen riesgo o conflicto

---

### 5. VerificationSummary.jsx - Resumen de verificación

**📍 Archivo:** `client/src/components/VerificationSummary.jsx`

#### Violación #10: Mostrar metadatos técnicos
**❌ BUSCAR:**
- IP del firmante
- Hash SHA-256
- Metadatos de archivo
- Algoritmos criptográficos

**✅ ELIMINAR** completamente del UI visible.

**✅ MOSTRAR SOLO:**
- Estado: Coincide / No coincide
- Fecha de certificación (formato humano: "15 de noviembre, 2024")
- Título del documento

**🔢 Mandamiento:** III - Nunca mostrar tecnicismos

---

## 🎯 PRIORIDAD MEDIA - Componentes Internos

### 6. SignatureWorkshop.jsx - Taller de firmas

**📍 Archivo:** `client/src/components/SignatureWorkshop.jsx`

#### Violación #11: Mencionar "firma criptográfica"
**❌ BUSCAR:**
```jsx
"Firma criptográfica generada"
"Clave privada utilizada"
```

**✅ REEMPLAZAR:**
```jsx
"Firma aplicada correctamente"
"Tu firma ha sido registrada"
```

**🔢 Mandamiento:** III - Nunca mostrar tecnicismos

---

### 7. DocumentList.jsx - Lista de documentos

**📍 Archivo:** `client/src/components/DocumentList.jsx`

#### Violación #12: Columna "Hash" en tabla
**❌ BUSCAR:**
```jsx
<th>Hash</th>
<td>{doc.hash}</td>
```

**✅ ELIMINAR** la columna de hash.

**✅ DEJAR SOLO:**
- Nombre del documento
- Fecha de certificación
- Estado
- Acciones

**🔢 Mandamiento:** III - Nunca mostrar tecnicismos

---

### 8. LegalProtectionOptions.jsx - Opciones legales

**📍 Archivo:** `client/src/components/LegalProtectionOptions.jsx`

#### Violación #13: Switches de anclaje y timestamp
**❌ BUSCAR:**
```jsx
<Switch label="Timestamp RFC 3161" />
<Switch label="Anclaje en blockchain" />
<Switch label="Anclaje en Bitcoin" />
```

**✅ ELIMINAR COMPLETAMENTE** este componente si existe.

**🔢 Mandamiento:** IV - Nunca mezclar conceptos técnicos en el flujo

---

### 9. NdaAccessPage.jsx - Página de acceso NDA

**📍 Archivo:** `client/src/pages/NdaAccessPage.jsx`

#### Violación #14: Términos como "tracking" o "monitoreo"
**❌ BUSCAR:**
```jsx
"Tu acceso será monitoreado"
"Rastreamos tu actividad"
"Sistema de vigilancia activo"
```

**✅ REEMPLAZAR:**
```jsx
"Tu acceso a este documento quedó registrado de forma segura"
"Este acceso se guarda para protección de ambas partes"
```

**🔢 Mandamiento:** XIV - Nunca usar palabras invasivas

---

## 🎯 PRIORIDAD BAJA - Mensajes del Sistema

### 10. Mensajes de error generales

**📍 Archivo:** Cualquier componente con manejo de errores

#### Violación #15: Errores técnicos expuestos
**❌ BUSCAR:**
```jsx
"Error al computar hash SHA-256"
"Fallo en timestamp del servidor"
"Error en parseo de metadatos"
```

**✅ REEMPLAZAR:**
```jsx
"Algo no salió bien. Intentá nuevamente"
"No pudimos procesar tu archivo"
"Hubo un problema. Intentá en unos segundos"
```

**🔢 Mandamiento:** XV - Nunca usar palabras industriales o mecánicas

---

### 11. Tooltips y ayuda contextual

**📍 Archivo:** `client/src/components/Tooltip.jsx` y otros

#### Violación #16: Explicaciones técnicas
**❌ BUSCAR:**
```jsx
"El hash SHA-256 certifica la integridad criptográfica"
"Timestamp RFC 3161 con validez legal"
```

**✅ REEMPLAZAR:**
```jsx
"Tu archivo .ECO contiene todas las pruebas de autenticidad"
"Podés compartir tu .ECO sin exponer el contenido original"
```

**🔢 Mandamiento:** III - Nunca mostrar tecnicismos

---

## 📦 CAMBIOS EN LIBRERÍAS (Solo comentarios internos)

### 12. basicCertificationWeb.js

**📍 Archivo:** `client/src/lib/basicCertificationWeb.js`

**⚠️ NOTA:** Este archivo es interno, NO se muestra al usuario.

**PERMITIDO:**
- Usar términos técnicos en comentarios de código
- Mencionar SHA-256, RFC 3161, blockchain en logs de consola

**NO PERMITIDO:**
- Exponer estos términos en strings que se muestran en UI
- Pasar mensajes técnicos a componentes de React

---

## ✅ CHECKLIST DE IMPLEMENTACIÓN

### Fase 1: Búsqueda y Reemplazo Global
- [ ] Buscar "subir" → reemplazar con "elegir" o "seleccionar"
- [ ] Buscar "hash" → eliminar de UI
- [ ] Buscar "SHA-256" → eliminar de UI
- [ ] Buscar "blockchain" → eliminar de UI
- [ ] Buscar "timestamp" → reemplazar con "sellado de fecha" o eliminar
- [ ] Buscar "RFC 3161" → eliminar de UI
- [ ] Buscar "anclaje" / "anclar" → eliminar de UI
- [ ] Buscar "firma criptográfica" → reemplazar con "firma"
- [ ] Buscar "manipulación" → reemplazar con "no coincide"
- [ ] Buscar "falsificación" → reemplazar con "no coincide"
- [ ] Buscar "fraude" → eliminar
- [ ] Buscar "procesar" → reemplazar con "preparar"
- [ ] Buscar "computar" → reemplazar con "calcular" o eliminar
- [ ] Buscar "público" → reemplazar con "compartido"
- [ ] Buscar "expuesto" → eliminar
- [ ] Buscar "monitoreo" / "rastreo" / "vigilancia" → reemplazar con "registrado"

### Fase 2: Componentes Específicos
- [ ] **Login.jsx** - Limpiar de fondos azules
- [ ] **Dashboard.jsx** - Quitar fondo azul de header, simplificar KPIs
- [ ] **CertificationFlow.jsx** - Eliminar paso de "Sellar evidencia"
- [ ] **CertificationFlow.jsx** - Cambiar mensajes de progreso
- [ ] **VerifyPage.jsx** - Eliminar detalles técnicos
- [ ] **VerificationSummary.jsx** - Solo mostrar: Coincide/No coincide + fecha
- [ ] **SignatureWorkshop.jsx** - Eliminar referencias a "firma criptográfica"
- [ ] **DocumentList.jsx** - Eliminar columna de hash
- [ ] **LegalProtectionOptions.jsx** - Eliminar switches técnicos (o eliminar componente)
- [ ] **NdaAccessPage.jsx** - Cambiar "monitoreo" por "registrado"
- [ ] **LandingPageV2.jsx** - Simplificar textos de Hero y "Cómo funciona"

### Fase 3: Estilos y Colores
- [ ] Crear variables CSS según DESIGN_SYSTEM.md
- [ ] Reemplazar `bg-blue-500` con `bg-accent` en botones primarios
- [ ] Reemplazar fondos azules grandes con `bg-white border border-soft`
- [ ] Eliminar rojos fuertes, usar `border-gray-400` para errores
- [ ] Unificar tipografía: `text-main` para títulos, `text-muted` para secundarios
- [ ] Asegurar que todos los botones usan solo 2 estilos: primario y secundario

### Fase 4: Validación Final
- [ ] Hacer búsqueda global de cada palabra prohibida
- [ ] Revisar cada pantalla contra checklist del DESIGN_SYSTEM.md
- [ ] Confirmar que ROL A (owner) y ROL B (invitado) no se mezclan
- [ ] Verificar que NO aparezcan procesos técnicos internos
- [ ] Probar flujo completo: Login → Certificar → Verificar → NDA

---

## 🚨 PALABRAS PROHIBIDAS - REFERENCIA RÁPIDA

### ❌ BUSCAR Y ELIMINAR/REEMPLAZAR:

**Generan miedo:**
- cualquiera → "otras personas"
- público → "compartido"
- expuesto → "disponible"
- subir / subido → "elegir" / "seleccionar"
- guardar en nuestros servidores → "guardar en tu cuenta"
- bloquear → "desactivar"
- intervenir → "modificar"

**Tecnicismos:**
- hash → eliminar
- SHA-256 → eliminar
- RFC 3161 → eliminar
- timestamp → "sellado de fecha y hora" o eliminar
- blockchain → eliminar
- Bitcoin / Polygon → eliminar
- anclaje / anclar → eliminar
- firma criptográfica → "firma"
- IP del firmante → eliminar
- metadatos → eliminar

**Riesgo/Conflicto:**
- fraude → eliminar
- manipulación → "no coincide"
- falsificación → "no coincide"
- disputa → "diferencia"
- amenaza → eliminar
- vulnerabilidad → "problema"
- irreversible → eliminar

**Industriales:**
- procesar → "preparar"
- computar → eliminar
- parsear → eliminar
- indexar → eliminar
- despliegue → eliminar
- compilar → eliminar

**Invasivas:**
- monitoreo → "registrado"
- rastreo → "registrado"
- vigilancia → "registro"
- seguimiento → "registro"
- tracking → "registro" (excepto "VerifyTracker" como nombre de producto)

---

## 📊 RESUMEN EJECUTIVO

**Total de violaciones encontradas:** 16 críticas
**Archivos afectados:** ~12 componentes principales
**Tiempo estimado de corrección:** 4-6 horas

**Prioridad de ejecución:**
1. ✅ Landing Page (impacto en conversión)
2. ✅ Dashboard y CertificationFlow (experiencia core)
3. ✅ VerifyPage (experiencia invitado)
4. ⚠️ Componentes internos (menor impacto UX)

---

**Próximo paso:** Implementar cambios siguiendo el checklist de Fase 1 → Fase 2 → Fase 3 → Fase 4.
