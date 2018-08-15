<template>
  <div id="app">
    <div 
      v-html="html">
    </div>
  </div>
</template>

<script>
  import marked from 'marked'

export default {
  name: 'app',
  data () {
    return {
      markdown: `La risposta è **sì** e, per fortuna, in molti casi si tratta di soluzioni **gratuite**.
Prima di scegliere uno strumento, però, è sempre bene chiedersi **per cosa lo si usa**. Cosa dovete comunicare, in che modo e a chi dovete comunicarlo?
Avere la risposta a queste domande può aiutare nell’adozione dello strumento più adatto ai vostri **scopi**.

# 1. Newsletter e Mailing List
Una mailing list è una lista dove vengono salvati i nominativi e gli indirizzi e-mail di tutti coloro che hanno deciso di iscriversi. L’iscrizione può essere eseguita dal diretto interessato o può esserci un responsabile addetto alla raccolta delle mail e al loro inserimento nella lista.

Una volta creata la lista, si può creare e inoltrare ai membri un’unica mail per tutti.

Ci sono diversi servizi che si occupano di inserire le mail raccolte in una lista e che permettono anche di creare mail e inviarle: Google Gruppi e MailChimp sono due servizi che permettono di farlo in maniera gratuita, fornendo anche diversi dati su quante persone hanno letto la vostra mail.

**Pro:**
1. Puoi mantenere aggiornati tutti gli iscritti in contemporanea,
2. Puoi scrivere una sola mail per tutti,
3. Puoi comunicare diverse cose in un’unica mail.

**Contro:**
1. Non puoi avviare conversazioni centralizzate,
2. Se molti rispondono alla mail, poi è difficile gestire le conversazioni.


# 2. Gruppi su Facebook
Facebook permette di creare **gruppi**, che possono essere aperti o chiusi, all’interno dei quali le comunicazioni sono singoli post che i membri possono commentare anche in diretta. Ogni post permette di raggruppare le conversazioni.

**Pro:**
1. Puoi permettere alle persone di commentare e partecipare attivamente in conversazioni,
2. I post permettono di raggruppare le conversazioni,
3. Puoi creare gruppi chiusi e aperti,
4. Puoi mantenere aggiornati tutti in contemporanea.

**Contro:**
1. Non si possono suddividere i post in tematiche

# 3. Slack
Su Slack c’è una pagina unica dell’organizzazione all’interno della quale, segnalati da un hashtag (il simbolo “#”), ci diversi canali. I canali sono spazi con tematiche diverse: ci sono canali per le informazioni generali, canali per gli eventi, canali per i progetti e molto altro.

**Pro:**
1. Puoi creare canali per tematiche 
2. I canali sono raggruppati nel gruppo più grande dell’organizzazione: tutto è centralizzato.
3. Puoi permettere alle persone di commentare e partecipare attivamente alle conversazioni,
4. I post permettono di raggruppare le conversazioni,
5. Puoi creare canali chiusi e aperti.

**Contro:**
1. Anche se i canali permettono di suddividere in tematiche le conversazioni, i singoli canali sono un unico flusso di messaggi e molte informazioni possono essere perse,
2. I canali sono come sottogruppi: più canali ci sono, più c’è il rischio di arrivare a un eccesso di messaggi e notifiche.

# 4. Comunicazioni istantanee
I servizi di messaggistica come Whatsapp, Telegram e Messenger (ma ce ne sono molti altri) permettono di creare gruppi anche con molte persone e possono essere usati per comunicazioni immediate.

**Pro:**
1. Informazioni veloci e immediate
2. Puoi informare tutti contemporaneamente
3. Puoi permettere alle persone di commentare e partecipare attivamente in una conversazioni

**Contro:**
1. La conversazione è un unico flusso e spesso molte informazioni possono venir perse o essere difficili da recuperare,
2. Più persone ci sono nel gruppo, più c’è il rischio che ai messaggi importanti ci siano mescolati anche messaggi superflui o che ci siano troppi messaggi in arrivo.

Il bello di questi strumenti è che uno non esclude l’altro: possono essere usati anche tutti assieme.

**L’importante è tenere presente come si vuole strutturare la comunicazione e che obiettivi si hanno.**`,
      html: ''
    }
  },
  created() {
    this.transform(this.markdown)
  },
  methods: {
     transform: function (markdown) {
      this.html = marked(markdown, { sanitize: true })
      console.log(this.html)
    }
  }
}
</script>

<style>
</style>
