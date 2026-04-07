---
title: Progetto Alpha
tags: [lavoro, progetto, python]
date: 2026-04-07
---

# Progetto Alpha

Nota di prova per testare vari elementi di rendering in Quartz.

## Stato

> [!NOTE] Questa è una callout di tipo NOTE
> Le callout di Obsidian sono supportate da Quartz.

> [!WARNING] Questa è una callout WARNING
> Utile per segnalare attenzioni nel sito pubblicato.

## Checklist di test

- [x] Wikilink verso la homepage [[../index|Home]]
- [x] Wikilink verso l'indice sezione [[index|Indice Lavoro]]
- [x] Tag nel frontmatter
- [ ] Immagine (vedi sotto — manca il file, testa il comportamento)
- [ ] Codice inline e blocchi di codice

## Blocco di codice

Questo testa il syntax highlighting:

```python
def aggiorna_sito(sorgente: str, destinazione: str) -> None:
    """Copia le note da @pubblico a content/ e fa git push."""
    import subprocess
    import shutil

    shutil.copytree(sorgente, destinazione, dirs_exist_ok=True)
    subprocess.run(["git", "add", "."], check=True)
    subprocess.run(["git", "commit", "-m", "Aggiornamento note"], check=True)
    subprocess.run(["git", "push"], check=True)
    print("Sito aggiornato.")
```

```bash
# Equivalente bash — testa anche l'highlight per shell
npx quartz build --serve
npx quartz sync
```

## Tabella

| Campo       | Valore              | Note                        |
|-------------|---------------------|-----------------------------|
| Nome        | Progetto Alpha      | Testa rendering tabelle     |
| Stato       | In corso            |                             |
| Priorità    | Alta                | Verificare in mobile        |

## Immagine di prova

Il file immagine non esiste — questo testa cosa mostra Quartz con un'immagine mancante:

![[immagine-test.png]]

Per testare un'immagine reale, aggiungere un file .png o .jpg nella cartella
@pubblico/lavoro/ con lo stesso nome e verificare che appaia nel sito.

## Link verso altre sezioni

- [[../personale/letture|Lista letture]] — link cross-sezione
