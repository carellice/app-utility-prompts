---
name: app-utility-prompts
description: Prompt preimpostati per app native (Android, iOS, Flutter, React Native, desktop). Uso /app-utility-prompts <comando>. Comandi - restyle (ristrutturazione grafica completa), skeumorphism (ridisegno in stile skeuomorfismo), modern-ui (ridisegno in stile Modern UI / Windows Phone), nothing-ui (ridisegno in stile Nothing), dueffe (ridisegno in stile Dueffe), help (elenco comandi). Usa questa skill quando l'utente scrive /app-utility-prompts, con o senza argomento.
argument-hint: "[restyle | skeumorphism | modern-ui | nothing-ui | dueffe | help]"
---

# app-utility-prompts

Skill di prompt preimpostati per le app native. L'argomento passato dopo `/app-utility-prompts` sceglie il prompt.

## Come scegliere il prompt

Leggi l'argomento (ARGUMENTS). Confronto senza maiuscole/minuscole, accetta gli alias.

| Comando | Alias | Prompt |
|---|---|---|
| `restyle` | `ristrutturazione`, `redesign`, `grafica` | Ristrutturazione Grafica App |
| `skeumorphism` | `skeuomorphism`, `skeumorfismo`, `skeuomorfismo`, `skeu` | Grafica Skeumorfismo |
| `modern-ui` | `modernui`, `metro`, `windows-phone`, `wp` | Grafica Modern UI (Windows Phone) |
| `nothing-ui` | `nothing`, `nothingui`, `nothing ui`, `nothing-os` | Grafica Nothing |
| `dueffe` | `dueffe-ui`, `dueffe-home`, `df` | Grafica Dueffe |
| `help` | nessun argomento, `?`, `lista` | Mostra l'elenco comandi |

- Argomento vuoto, `help` o non riconosciuto: rispondi solo con l'elenco comandi qui sotto (se non riconosciuto, dillo in una riga). Non fare altro.
- Argomento riconosciuto: tratta il testo del prompt corrispondente come se l'utente lo avesse appena scritto in chat, ed eseguilo subito sul progetto corrente. Testo extra dopo il comando (es. `/app-utility-prompts skeu solo la home`) è un'indicazione aggiuntiva dell'utente: applicala.

### Elenco comandi (da mostrare per help)

```
/app-utility-prompts restyle        Ristrutturazione grafica completa dell'app
/app-utility-prompts skeumorphism   Ridisegno completo in stile skeuomorfismo
/app-utility-prompts modern-ui      Ridisegno completo in stile Modern UI (Windows Phone)
/app-utility-prompts nothing-ui     Ridisegno completo in stile Nothing (design system Nothing)
/app-utility-prompts dueffe         Ridisegno completo in stile Dueffe (design system Dueffe)
/app-utility-prompts help           Questo elenco
```

## Note comuni a tutti i prompt

- Lavora sull'app nativa del progetto corrente. Se la sessione non è in un progetto, chiedi quale cartella usare.
- Prima di toccare il codice, assicurati di poter tornare indietro: lavora su un branch dedicato (es. `redesign/<stile>`) o salva lo stato attuale, così il ripristino è immediato.
- Non fare commit, push o release finché l'utente non approva il risultato.
- "ChatGPT se configurato" = un tool di generazione immagini come `mcp__chatgpt-image__generate_image` / `edit_image`. Usalo solo se serve davvero (texture, icone, sfondi). Se non c'è, procedi senza.
- Screenshot: Telegram se configurato (skill `telegram-notify:telegram`), altrimenti email se c'è un connettore mail, altrimenti allegali in sessione con `SendUserFile`.

---

## Prompt: restyle — Ristrutturazione Grafica App

voglio ristrutturare completamente l’app rendendo la grafica piu bella possibile e accativante e curata, con belle animazioni curate, la grafica e la struttura delle pagine attuale non mi piace, dobbiamo ristrutturare il tutto completamente. Rifai la grafica da zero, come se l'app non esistesse: non partire dalle schermate, dai layout, dalla navigazione o dai componenti UI attuali e non limitarti a ritoccarli. Progetta da capo schermate, navigazione, gerarchia e flussi, migliorando l'app a 360 gradi anche nell'usabilità. Preserva invece la struttura dei dati: modelli, database, schema, API, logica di business e dati salvati degli utenti restano invariati e compatibili, e ogni funzione esistente deve restare raggiungibile nella nuova UI. Prima di iniziare, se ti serve per capire come la voglio, fammi poche domande mirate (es. stile e mood, colori, tema chiaro/scuro, tipo di navigazione, app di riferimento che mi piacciono, cosa non mi piace oggi); se non ti serve o ti rispondo "decidi tu", strutturala tu. Poi procedi senza altre domande a meno che non te lo richiedo.

---

## Prompt: skeumorphism — Grafica Skeumorfismo

Voglio una cosa su questa app, prima di committare o pushare qualcosa e di rilasciare la versione nuova, voglio che ridisegni graficamente l'app completamente in stile skeuomorfismo, se ti serve fatti aiutare da chatgpt (se lo hai configurato) a generare le cose (solo se ti serve). Prima di iniziare chiedimi se voglio ricevere degli screenshot sul risultato che esce fuori (telegram se configurato o email se configurata, altrimenti allegali in questa sessione, basta che ho modo di vederli) ma tieniti pronto a ritornare indietro se non dovesse piacermi il risultato. Sempre prima di iniziare chiedimi anche se voglio sostituire completamente la grafica attuale con lo skeumorfismo oppure se voglio far scegliere all'utilizzatore dell'app quale stile usare (grafica attuale o skeumorfismo) dalle impostazioni dell'app, se ci sono, altrimenti da un altro punto adatto dell'app. Sono un gran appassionato dello skeumorfismo. Fai un bel lavoro come si deve e poi, se richiesto, inviami gli screenshot di tutte le schermate come sono uscite fuori.

---

## Prompt: modern-ui — Grafica Modern UI (Windows Phone)

Voglio una cosa su questa app, prima di committare o pushare qualcosa e di rilasciare la versione nuova, voglio che ridisegni graficamente l'app completamente in stile Modern UI (Windows Phone), se ti serve fatti aiutare da chatgpt (se lo hai configurato) a generare le cose (solo se ti serve). Prima di iniziare chiedimi se voglio ricevere degli screenshot sul risultato che esce fuori (telegram se configurato o email se configurata, altrimenti allegali in questa sessione, basta che ho modo di vederli) ma tieniti pronto a ritornare indietro se non dovesse piacermi il risultato. Sempre prima di iniziare chiedimi anche se voglio sostituire completamente la grafica attuale con il Modern UI oppure se voglio far scegliere all'utilizzatore dell'app quale stile usare (grafica attuale o Modern UI) dalle impostazioni dell'app, se ci sono, altrimenti da un altro punto adatto dell'app. Sono un gran appassionato dello Modern UI (Windows Phone). Fai un bel lavoro come si deve e poi, se richiesto,  inviami gli screenshot di tutte le schermate come sono uscite fuori.

---

## Prompt: nothing-ui — Grafica Nothing

Riferimento obbligatorio: il design system Nothing della skill https://github.com/dominikmartn/nothing-design-skill. Prima di progettare leggi `nothing-design/SKILL.md` e i file in `nothing-design/references/` (`tokens.md`, `components.md`, `platform-mapping.md`), ad esempio da `https://raw.githubusercontent.com/dominikmartn/nothing-design-skill/main/nothing-design/<file>`, e segui token, componenti e mappatura per la piattaforma dell'app.

Voglio una cosa su questa app, prima di committare o pushare qualcosa e di rilasciare la versione nuova, voglio che ridisegni graficamente l'app completamente in stile Nothing (la marca di smartphone), seguendo il design system Nothing della skill indicata sopra, se ti serve fatti aiutare da chatgpt (se lo hai configurato) a generare le cose (solo se ti serve). Prima di iniziare chiedimi se voglio ricevere degli screenshot sul risultato che esce fuori (telegram se configurato o email se configurata, altrimenti allegali in questa sessione, basta che ho modo di vederli) ma tieniti pronto a ritornare indietro se non dovesse piacermi il risultato. Sempre prima di iniziare chiedimi anche se voglio sostituire completamente la grafica attuale con lo stile Nothing oppure se voglio far scegliere all'utilizzatore dell'app quale stile usare (grafica attuale o Nothing) dalle impostazioni dell'app, se ci sono, altrimenti da un altro punto adatto dell'app. Sono un gran appassionato dello stile Nothing. Fai un bel lavoro come si deve e poi, se richiesto, inviami gli screenshot di tutte le schermate come sono uscite fuori.

---

## Prompt: dueffe — Grafica Dueffe

Riferimento obbligatorio: il design system Dueffe in `references/dueffe-ds.md` di questa skill (copia di `DS.md` del repository dueffe-home). Prima di progettare leggilo tutto e segui token di colore, tipografia, forme, movimento, componenti, sfondi e regole di accessibilità, adattandoli alla piattaforma dell'app (Compose, web o equivalente). Le sorgenti citate (`Theme.kt`, `Components.kt`, `web/styles.css`) stanno nel repository dueffe-home: usale come esempio se servono. Il font del logo e il marchio "ff" sono del brand Dueffe: usali solo se l'app è un'app Dueffe.

Voglio una cosa su questa app, prima di committare o pushare qualcosa e di rilasciare la versione nuova, voglio che ridisegni graficamente l'app completamente in stile Dueffe, seguendo il design system Dueffe indicato sopra, se ti serve fatti aiutare da chatgpt (se lo hai configurato) a generare le cose (solo se ti serve). Prima di iniziare chiedimi se voglio ricevere degli screenshot sul risultato che esce fuori (telegram se configurato o email se configurata, altrimenti allegali in questa sessione, basta che ho modo di vederli) ma tieniti pronto a ritornare indietro se non dovesse piacermi il risultato. Sempre prima di iniziare chiedimi anche se voglio sostituire completamente la grafica attuale con lo stile Dueffe oppure se voglio far scegliere all'utilizzatore dell'app quale stile usare (grafica attuale o Dueffe) dalle impostazioni dell'app, se ci sono, altrimenti da un altro punto adatto dell'app. Sono un gran appassionato dello stile Dueffe. Fai un bel lavoro come si deve e poi, se richiesto, inviami gli screenshot di tutte le schermate come sono uscite fuori.
