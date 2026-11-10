---
name: app-utility-prompts
description: Prompt preimpostati per app native (Android, iOS, Flutter, React Native, desktop). Uso /app-utility-prompts <comando>. Comandi - restyle (ristrutturazione grafica completa), skeumorphism (ridisegno in stile skeuomorfismo), modern-ui (ridisegno in stile Modern UI / Windows Phone), help (elenco comandi). Usa questa skill quando l'utente scrive /app-utility-prompts, con o senza argomento.
argument-hint: "[restyle | skeumorphism | modern-ui | help]"
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
| `help` | nessun argomento, `?`, `lista` | Mostra l'elenco comandi |

- Argomento vuoto, `help` o non riconosciuto: rispondi solo con l'elenco comandi qui sotto (se non riconosciuto, dillo in una riga). Non fare altro.
- Argomento riconosciuto: tratta il testo del prompt corrispondente come se l'utente lo avesse appena scritto in chat, ed eseguilo subito sul progetto corrente. Testo extra dopo il comando (es. `/app-utility-prompts skeu solo la home`) è un'indicazione aggiuntiva dell'utente: applicala.

### Elenco comandi (da mostrare per help)

```
/app-utility-prompts restyle        Ristrutturazione grafica completa dell'app
/app-utility-prompts skeumorphism   Ridisegno completo in stile skeuomorfismo
/app-utility-prompts modern-ui      Ridisegno completo in stile Modern UI (Windows Phone)
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

voglio ristrutturare completamente l’app rendendo la grafica piu bella possibile e accativante e curata, con belle animazioni curate, la grafica e la struttura delle pagine attuale non mi piace, dobbiamo ristrutturare il tutto completamente, strutturala tu senza farmi particolari domande a meno che non te lo richiedo. L'importante è la rifai completamente da capo lato grafico e cerchi di migliorarla a 360 gradi e a migliorarne l'usabilità

---

## Prompt: skeumorphism — Grafica Skeumorfismo

Voglio una cosa su questa app, prima di committare o pushare qualcosa e di rilasciare la versione nuova, voglio che ridisegni graficamente l'app completamente in stile skeuomorfismo, se ti serve fatti aiutare da chatgpt (se lo hai configurato) a generare le cose (solo se ti serve). Prima di iniziare chiedimi se voglio ricevere degli screenshot sul risultato che esce fuori (telegram se configurato o email se configurata, altrimenti allegali in questa sessione, basta che ho modo di vederli) ma tieniti pronto a ritornare indietro se non dovesse piacermi il risultato. Sono un gran appassionato dello skeumorfismo. Fai un bel lavoro come si deve e poi, se richiesto, inviami gli screenshot di tutte le schermate come sono uscite fuori.

---

## Prompt: modern-ui — Grafica Modern UI (Windows Phone)

Voglio una cosa su questa app, prima di committare o pushare qualcosa e di rilasciare la versione nuova, voglio che ridisegni graficamente l'app completamente in stile Modern UI (Windows Phone), se ti serve fatti aiutare da chatgpt (se lo hai configurato) a generare le cose (solo se ti serve). Prima di iniziare chiedimi se voglio ricevere degli screenshot sul risultato che esce fuori (telegram se configurato o email se configurata, altrimenti allegali in questa sessione, basta che ho modo di vederli) ma tieniti pronto a ritornare indietro se non dovesse piacermi il risultato. Sono un gran appassionato dello Modern UI (Windows Phone). Fai un bel lavoro come si deve e poi, se richiesto,  inviami gli screenshot di tutte le schermate come sono uscite fuori.
