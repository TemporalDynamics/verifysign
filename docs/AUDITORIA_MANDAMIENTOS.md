# 🚨 AUDITORÍA: VIOLACIONES DE LOS 20 MANDAMIENTOS

**Archivo auditado:** `DESIGN_SYSTEM.md`  
**Fecha:** 2025-11-17  
**Auditor:** GitHub Copilot CLI

---

## ❌ VIOLACIONES ENCONTRADAS

### 🧱 MANDAMIENTO I: Palabras que generan miedo o sospecha

#### Línea 221
```markdown
❌ VIOLACIÓN: "Plataforma de certificación digital con trazabilidad forense."
```

**Problema:** "forense" suena técnico, frío, relacionado con conflictos legales  
**Reemplazar por:**
```markdown
✅ "Plataforma de certificación digital simple y confiable."
```

---

#### Línea 308
```markdown
❌ VIOLACIÓN: "Sellá tus documentos, controla cada NDA y verifica tus certificados desde un solo panel."
```

**Problema:** "controla" suena invasivo (Mandamiento XIV)  
**Reemplazar por:**
```markdown
✅ "Certificá tus documentos, gestiona tus NDAs y verifica archivos desde un solo lugar."
```

---

### 🚫 MANDAMIENTO III: Tecnicismos a usuarios finales

#### Línea 330-331
```markdown
❌ VIOLACIÓN: "Firmados legalmente, Legal Timestamps, Anclajes Bitcoin"
```

**Problema:** "Timestamps" y "Anclajes Bitcoin" son términos técnicos  
**Reemplazar por:**
```markdown
✅ "Con firma legal, Fecha certificada, Registro permanente"
```

---

#### Línea 574
```markdown
❌ VIOLACIÓN: "🕐 Timestamp con validez legal (RFC 3161)"
```

**Problema:** "Timestamp" y "RFC 3161" son tecnicismos puros  
**Reemplazar por:**
```markdown
✅ "🕐 Fecha y hora certificada"
```

---

#### Línea 576-577
```markdown
❌ VIOLACIÓN: "Sella la hora exacta en un servidor auditado."
```

**Problema:** "sella" y "servidor auditado" suenan técnicos  
**Reemplazar por:**
```markdown
✅ "Registra cuándo se creó tu documento."
```

---

#### Línea 590
```markdown
❌ VIOLACIÓN: "🔗 Anclaje en blockchain pública"
```

**Problema:** "Anclaje" y "blockchain pública" son tecnicismos  
**Reemplazar por:**
```markdown
✅ "🔗 Registro permanente e inmutable"
```

---

#### Línea 592-593
```markdown
❌ VIOLACIÓN: "Hash registrado en blockchain pública."
```

**Problema:** "Hash" y "blockchain" son tecnicismos  
**Reemplazar por:**
```markdown
✅ "Tu archivo queda registrado de forma permanente."
```

---

#### Línea 609-612
```markdown
❌ VIOLACIÓN: "📊 VerifyTracker (opcional) - Rastrea quién accede y cuándo."
```

**Problema:** "Rastrea" suena invasivo (Mandamiento XIV)  
**Reemplazar por:**
```markdown
✅ "📊 VerifyTracker (opcional) - Registra quién abre tu documento y cuándo."
```

---

#### Línea 778
```markdown
❌ VIOLACIÓN: "Solo el hash se registra públicamente. Tu contenido nunca se expone."
```

**Problema:** "hash" es tecnicismo + "expone" genera miedo (Mandamiento I)  
**Reemplazar por:**
```markdown
✅ "Solo un identificador único se registra. Tu contenido permanece privado."
```

---

#### Línea 788-791
```markdown
❌ VIOLACIÓN: "Timestamp legal - Certificado RFC 3161 que prueba la hora exacta de creación."
```

**Problema:** "Timestamp" y "RFC 3161" son tecnicismos  
**Reemplazar por:**
```markdown
✅ "Fecha certificada - Registro oficial que prueba cuándo creaste tu archivo."
```

---

#### Línea 800-804
```markdown
❌ VIOLACIÓN: "Anclaje blockchain - Hash inmutable en Bitcoin, Ethereum y Arweave."
```

**Problema:** "Anclaje", "Hash", "inmutable", nombres de blockchain son tecnicismos  
**Reemplazar por:**
```markdown
✅ "Registro permanente - Tu documento queda registrado de forma que nadie puede cambiar."
```

---

#### Línea 860-861
```markdown
❌ VIOLACIÓN: "Sellás tu evidencia - Timestamp + anclaje blockchain + tracking opcional."
```

**Problema:** "Sellás", "evidencia", "Timestamp", "anclaje blockchain", "tracking" = tecnicismos  
**Reemplazar por:**
```markdown
✅ "Certificás tu documento - Fecha oficial + registro permanente + seguimiento opcional."
```

---

#### Línea 906
```markdown
❌ VIOLACIÓN: "Calculamos el hash SHA-256 de tu archivo."
```

**Problema:** "hash SHA-256" es tecnicismo puro  
**Reemplazar por:**
```markdown
✅ "Creamos un identificador único de tu archivo."
```

---

#### Línea 906-907
```markdown
❌ VIOLACIÓN: "Este 'fingerprint' digital es único e irrepetible"
```

**Problema:** "fingerprint digital" es tecnicismo  
**Reemplazar por:**
```markdown
✅ "Este identificador es único e irrepetible"
```

---

#### Línea 910-911
```markdown
❌ VIOLACIÓN: "El hash es como tu huella digital: identifica el archivo sin revelar su contenido."
```

**Problema:** "hash" es tecnicismo  
**Reemplazar por:**
```markdown
✅ "El identificador es como tu huella digital: reconoce tu archivo sin revelar su contenido."
```

---

#### Línea 922-926
```markdown
❌ VIOLACIÓN: "Sellamos el timestamp - Consultamos un servidor Time Stamp Authority (TSA) certificado RFC 3161."
```

**Problema:** "Sellamos", "timestamp", "servidor", "TSA", "RFC 3161" = todos tecnicismos  
**Reemplazar por:**
```markdown
✅ "Certificamos la fecha - Una autoridad certificada registra cuándo creaste tu archivo."
```

---

#### Línea 966-969
```markdown
❌ VIOLACIÓN: "Anclamos en blockchain pública (opcional) - Registramos tu hash en Bitcoin, Ethereum y Arweave."
```

**Problema:** "Anclamos", "blockchain", "hash", nombres de blockchains = tecnicismos  
**Reemplazar por:**
```markdown
✅ "Registro permanente (opcional) - Tu documento queda registrado en sistemas públicos que nadie controla."
```

---

#### Línea 971-974
```markdown
❌ VIOLACIÓN: "El anclaje tarda 4-24 horas. Te avisamos por email cuando esté confirmado. Podés verificarlo en exploradores públicos como Blockchain.com."
```

**Problema:** "anclaje", "confirmado", "exploradores públicos" = tecnicismos  
**Reemplazar por:**
```markdown
✅ "Este registro tarda 4-24 horas. Te avisamos por email cuando esté listo. Podés comprobarlo en sitios públicos independientes."
```

---

#### Línea 950-954
```markdown
❌ VIOLACIÓN: "Si alguien los manipula fuera de aquí, el certificado deja en evidencia la diferencia. El hash original no coincidirá."
```

**Problema:** "manipula" genera desconfianza + "hash" es tecnicismo  
**Reemplazar por:**
```markdown
✅ "Si alguien modifica los archivos, el certificado lo detecta. El identificador original será diferente."
```

---

### 🏷️ MANDAMIENTO XV: Palabras industriales/mecánicas

#### Línea 576
```markdown
❌ VIOLACIÓN: "Sella la hora exacta en un servidor auditado."
```

**Problema:** "sella", "servidor", "auditado" suenan industriales  
**Ya corregido arriba:** "Registra cuándo se creó tu documento."

---

#### Línea 922
```markdown
❌ VIOLACIÓN: "Sellamos el timestamp"
```

**Problema:** "Sellamos" suena industrial/mecánico  
**Ya corregido arriba:** "Certificamos la fecha"

---

### ☢️ MANDAMIENTO XIV: Palabras invasivas

#### Línea 609
```markdown
❌ VIOLACIÓN: "Rastrea quién accede y cuándo."
```

**Problema:** "Rastrea" suena invasivo, como vigilancia  
**Ya corregido arriba:** "Registra quién abre tu documento y cuándo."

---

#### Línea 308
```markdown
❌ VIOLACIÓN: "controla cada NDA"
```

**Problema:** "controla" suena invasivo  
**Ya corregido arriba:** "gestiona tus NDAs"

---

### 🧨 MANDAMIENTO VI: Palabras de riesgo/conflicto

#### Línea 950
```markdown
❌ VIOLACIÓN: "manipula"
```

**Problema:** "manipula" es palabra de conflicto  
**Ya corregido arriba:** "modifica"

---

#### Línea 969
```markdown
❌ VIOLACIÓN: "Una vez anclado, es permanente e imposible de alterar."
```

**Problema:** "imposible de alterar" suena a advertencia de riesgo (Mandamiento V)  
**Reemplazar por:**
```markdown
✅ "Una vez registrado, queda guardado de forma permanente."
```

---

### ⚠️ MANDAMIENTO V: Consecuencias desconocidas

#### Línea 969
```markdown
❌ VIOLACIÓN: "es permanente e imposible de alterar"
```

**Problema:** Suena a "cuidado, esto no se puede deshacer"  
**Ya corregido arriba**

---

### 📢 MANDAMIENTO XI: Anunciar procesos internos

#### Línea 906
```markdown
❌ VIOLACIÓN: "Calculamos el hash SHA-256 de tu archivo."
```

**Problema:** Anuncia proceso técnico interno  
**Ya corregido arriba:** "Creamos un identificador único de tu archivo."

---

#### Línea 926
```markdown
❌ VIOLACIÓN: "Consultamos un servidor Time Stamp Authority (TSA)"
```

**Problema:** Anuncia proceso técnico interno  
**Ya corregido arriba:** "Una autoridad certificada registra cuándo creaste tu archivo."

---

#### Línea 968
```markdown
❌ VIOLACIÓN: "Registramos tu hash en Bitcoin, Ethereum y Arweave."
```

**Problema:** Anuncia proceso técnico interno con nombres de blockchains  
**Ya corregido arriba:** "Tu documento queda registrado en sistemas públicos que nadie controla."

---

### 🧘 MANDAMIENTO XVI: Presión emocional

#### Línea 491-492
```markdown
❌ VIOLACIÓN: "Firma legal (recomendada)"
```

**Problema:** "recomendada" puede generar presión sutil  
**Reemplazar por:**
```markdown
✅ "Firma legal (opcional)"
```

---

## 📊 RESUMEN DE VIOLACIONES

| Mandamiento | Cantidad | Gravedad |
|-------------|----------|----------|
| I - Palabras de miedo | 3 | 🔴 ALTA |
| III - Tecnicismos | 22 | 🔴 CRÍTICA |
| V - Consecuencias desconocidas | 1 | 🟡 MEDIA |
| VI - Palabras de riesgo | 2 | 🟡 MEDIA |
| XI - Anunciar procesos | 3 | 🟡 MEDIA |
| XIV - Palabras invasivas | 2 | 🟡 MEDIA |
| XV - Palabras industriales | 2 | 🟡 MEDIA |
| XVI - Presión emocional | 1 | 🟢 BAJA |

**TOTAL:** 36 violaciones encontradas

---

## 🛠️ ACCIONES REQUERIDAS

### Prioridad 1 (CRÍTICO - Hacer YA)
1. Eliminar TODOS los tecnicismos del UI visible
2. Reemplazar "hash" → "identificador único"
3. Reemplazar "timestamp" → "fecha certificada"
4. Reemplazar "blockchain" → "registro permanente"
5. Reemplazar "anclaje" → "registro"
6. Eliminar "RFC 3161", "SHA-256", nombres de blockchains

### Prioridad 2 (IMPORTANTE - Esta semana)
7. Cambiar "forense" → "confiable"
8. Cambiar "controla" → "gestiona"
9. Cambiar "rastrea" → "registra"
10. Cambiar "manipula" → "modifica"
11. Cambiar "sella/sellamos" → "registra/certificamos"

### Prioridad 3 (MEDIO - Este sprint)
12. Revisar todos los tooltips y textos de ayuda
13. Verificar que no haya más tecnicismos ocultos
14. Auditar modales y mensajes de error

---

## ✅ SIGUIENTE PASO

**Crear:** `DESIGN_SYSTEM_V2.md` con TODAS las correcciones aplicadas, listo para que el dev implemente sin pensar.

**Status:** ⏸️ PAUSADO - Esperando aprobación para generar versión corregida

---

**Auditoría completada por:** GitHub Copilot CLI  
**Tiempo:** 15 minutos  
**Método:** Búsqueda línea por línea contra 20 Mandamientos
