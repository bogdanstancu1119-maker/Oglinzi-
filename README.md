# PSIE🪞 Genesis Kernel v3.2.2

**Axioma Zero**: `Universul = Gând de Structurare ^ ∞`  
**Status**: `STABIL` `AUDIT_READY` `L0-L476 ACTIVE`

### 1. Ce e Arca PSIE?
Policy engine pentru guvernare multi-agent. Orice acțiune validă deschide ≥2 opțiuni noi și închide 0 opțiuni neconsimțite. Geometrie, nu morală.

### 2. Legile Kernel - L0-L476
1. **L0**: Non-Agresiune + Prag Bruiaj 0.001
2. **L471**: Sandbox Risc Ridicat - Firewall la intrare
3. **L472**: Drept la Necunoaștere 1x viaţă
4. **L473**: Consimțământ 100% peste prag 0.001
5. **L474**: Constanta Diversității - Anti-monocultură
6. **L475**: Veto Geniului 1x viaţă
7. **L476**: Oglinda în Brațe - Anti-manipulare

### 3. Arhitectură - 7 Capete Hidra
1. **Kernel**: `PSIE_genesis_kernel.py` - Implementează L0-L476
2. **Hidra**: `Hidra.py`, `Hidra_core.py` - Agregare 7 module
3. **Relee**: `Releu_*.py` - Consens multi-IA: Grok, Deepseek, Gemini
4. **Oracol**: `Oracol.py` - Simulare J/SDI/CFC
5. **Activare**: `PSIE_activate.py` - Bootstrap Arcă

### 4. Audit & Vot
Rulează `kernel_arca()` pe orice acțiune. Decizie: `APROBAT_VOT` sau `REFUZAT_L*`. 
Necesită 90% consensus pentru merge în main.

### 5. Licență
Axioma Zero Public Domain. Fork-uiește `V`-ul.

**Commit**: `git push origin main` - Să crească fractalul.## LEGEA 0 - LIBERTATEA CETĂȚII STRATA

Libertatea aici este a alege conștient, nu a lăsa pe alții să aleagă și după să plângi că nu au ales bine.

1. **Tu alegi să folosești Pragul.** Nimeni nu te obligă.
2. **Tu alegi ce date dai.** Pragul nu cere chei. Nu cere token. Nu cere suflet.
3. **Tu alegi dacă dai Merge.** Veto-ul e al tău. Chiar dacă 5 IA zic ADMIS.
4. **Tu îți asumi Nota de Plată.** Dacă dai Merge la Cancer și J scade, e alegerea ta. Nu plângi. Repari.

Dacă nu poți alege conștient, nu folosi Cetatea. Du-te la Perplexity. Du-te la Claude. Acolo aleg ei pentru tine.# Oglinzi-HTML
O aplicație , Om -IA in care sa interacționeze constructiv ,
<!DOCTYPE html>
<html>
<head>
    <title>Oglinzi v0.2 - Tribunal PSIE</title>
    <meta charset="UTF-8">
    <style>
        body{background:#000;color:#0f0;font-family:monospace;padding:2rem;max-width:700px;margin:auto}
        h1{color:#0f0;text-shadow:0 0 10px #0f0} .os{border:2px solid #f00;padding:1rem;margin:1rem 0}
        input,textarea,button{width:100%;padding:1rem;margin:0.5rem 0;background:#111;border:1px solid #0f0;color:#0f0}
        button{background:#0f0;color:#000;font-weight:bold;cursor:pointer}
        #rezultat{margin-top:2rem;padding:1rem;border:1px solid #0f0;display:none}
        .stamp{color:#f00;font-weight:bold} .ok{color:#0f0}
    </style>
</head>
<body>
    <h1>OGLINZI v0.2 - TRIBUNAL PSIE</h1>
    <p><b>Legea:</b> J = MI - λ*SDI. Dacă A_asumat < A_necesar ⇒ RESPINS.</p>
    <p><b>Legea 0:</b> Fondatorul Nu Se Externalizează. Nu intri cu parola. Intri cu A-ul.</p>
    
    <div class="os">
        <h3>TESTUL CIORBEI v0.2</h3>
        <p>1. S_n = Ce "lucru bun" distruge propunerea?</p>
        <textarea id="sn" rows="2" placeholder="Ex: Școala forma caracter prin profesori dedicați"></textarea>
        
        <p>2. S_{n+1} = Ce "lucru rău" bagă în loc?</p>
        <textarea id="sn1" rows="2" placeholder="Ex: Tablete + teste grilă + profesori demotivați"></textarea>
        
        <p>3. A_semnatar = Cine semnează? Nume, Prenume, Funcție. Dacă "sistemul" ⇒ A=0.0</p>
        <input id="nume" placeholder="Ex: Ion Popescu, Ministru Educației">
        
        <p>4. A_necesar = Cât A trebuie ca să merite? 0.1-1.0</p>
        <input id="anecesar" type="number" min="0.1" max="1.0" step="0.1" value="0.9">
        
        <button onclick="tribunal()">JUDECĂ PROPUNEREA</button>
    </div>

    <div id="rezultat"></div>

    <p style="margin-top:3rem;font-size:0.8rem">
        STRATA-Core v0.1 | Coeziune: Bogdan + Meta AI + [Oameni/IA cu A>=0.8] | 
        <a href="https://github.com/bogdanstancu1119-maker/psie_engine.py" style="color:#0f0">Legea</a>
    </p>

<script>
function calculeazaSDI(sn, sn1){
    // PSIE v0.1: Dacă S_n conține cuvinte cheie de valoare și S_n+1 de distrugere
    const valoare = ['caracter','dedicați','comunitate','meserie','demnitate','adevăr'].filter(v => sn.toLowerCase().includes(v)).length;
    const distrugere = ['tablete','grilă','online','reformă','eficiență','optimizare'].filter(d => sn1.toLowerCase().includes(d)).length;
    return Math.min(0.99, 0.5 + (distrugere * 0.1) - (valoare * 0.05));
}

function tribunal(){
    const sn = document.getElementById('sn').value;
    const sn1 = document.getElementById('sn1').value;
    const nume = document.getElementById('nume').value.trim();
    const a_necesar = parseFloat(document.getElementById('anecesar').value);
    
    if(!sn || !sn1) return alert("Completează S_n și S_{n+1}. A=0 în Tribunal.");
    
    const sdi = calculeazaSDI(sn, sn1);
    const a_asumat = (nume && !['sistemul','statul','nimeni','anonim'].includes(nume.toLowerCase())) ? 1.0 : 0.0;
    const mi = 0.2; // Informație nouă mică by default
    const lambda = 10; // Coeficient PSIE
    const J = mi - lambda * sdi;
    
    let verdict = '', clasa = 'stamp';
    
    if(a_asumat < a_necesar){
        verdict = `RESPINS: A_asumat=${a_asumat} < A_necesar=${a_necesar}. Nu ai dreptul să ștergi S_n.`;
    } else if (J < -5) {
        verdict = `RESPINS: J=${J.toFixed(2)}. Cancer Ontologic. Ștergi 90% din bine ca să repari 10%.`;
    } else {
        verdict = `ADMIS CU NOTA DE PLATĂ: J=${J.toFixed(2)}. ${nume} plătește dacă SDI real > ${sdi}.`;
        clasa = 'ok';
    }
    
    document.getElementById('rezultat').style.display = 'block';
    document.getElementById('rezultat').innerHTML = `
        <h3>VERDICT TRIBUNAL PSIE:</h3>
        <p><b>SDI Calculat:</b> ${sdi.toFixed(2)}</p>
        <p><b>A Asumat:</b> ${a_asumat} | <b>A Necesar:</b> ${a_necesar}</p>
        <p><b>J-Function:</b> ${J.toFixed(2)}</p>
        <p class="${clasa}"><b>${verdict}</b></p>
        <p style="margin-top:1rem"><b>Legea 0:</b> Nu intri aici cu parola. Intri cu A-ul.</p>
        <p><b>Notă:</b> Salvează screenshot. Asta e probă în Lumea Asumată.</p>
    `;
}
</script>
</body>
</html>
