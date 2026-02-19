# Svelte:element 

## Installatie
- Open een code editor programma
- Clone de code van de repository main branch en zorg dat je 'contribute for my own purposes' aanklikt.
- Gebruik de main branche of maak een feature branche aan.
- Type in "npm install" zodat je de nodige dependencies download.
- Type in "npm run dev" of "npm run dev -- --open" zodat het project kan gestart worden.
- Klik op de local host als je npm run dev hebt gedaan en je ziet het project of het project start automatische op met npm run -- --open.

## Uitleg 
<svelte:element> is een speciaal onderdeel in Svelte waarmee je kunt kiezen welk HTML-element wordt gemaakt, zoals een h1, h2 of p.
In het <script> zet je eerst welk element standaard gebruikt wordt. Daarna kun je dit veranderen, zodat het element mee verandert terwijl de website draait.
In de HTML gebruik je <svelte:element> en verbind je het aan de variabele uit het script. Zo weet Svelte welk HTML-element het moet tonen.
Dit is handig omdat je componenten dan makkelijker herbruikbaar maakt.

## Voorbeeld 
### Dit is een klein component (atom)
<pre><code>
&lt;script&gt;
  let { as = "p" } = $props();
&lt;/script&gt;

&lt;svelte:element this={as}&gt;
  Svelte:element
&lt;/svelte:element&gt;
</code></pre>

### Dit is een groter component (molecule). 

<pre><code>
&lt;script&gt;
  import { Text } from "$lib/index.js";
&lt;/script&gt;

&lt;section&gt;
  &lt;img src="" alt="" height="100" width="250" /&gt;
  &lt;Text as="h2"&gt;&lt;/Text&gt;
  &lt;p&gt;
    Je kan hiermee kiezen welke html element je wil gebruiken. Zo kan je
    herbruikbare componenten maken.
  &lt;/p&gt;
&lt;/section&gt;
</code></pre>



### Dit is een nog grotere component (organisms)
<pre><code>
&lt;script&gt;
  import { ContainerCard } from "$lib/index.js";
&lt;/script&gt;

&lt;div&gt;
  &lt;ContainerCard&gt;&lt;/ContainerCard&gt;
  &lt;ContainerCard&gt;&lt;/ContainerCard&gt;
&lt;/div&gt;
</code></pre>


### Dit is de de pagina
<pre><code>
&lt;script&gt;
  import { Text, ContainerCards, Link, Ul } from "$lib/index.js";
&lt;/script&gt;

&lt;Text as="h1"&gt;&lt;/Text&gt;
&lt;Link&gt;&lt;/Link&gt;

&lt;ContainerCards&gt;&lt;/ContainerCards&gt;

&lt;Ul&gt;&lt;/Ul&gt;
</code></pre>

### Website 
<img width="1440" height="674" alt="Scherm­afbeelding 2026-02-19 om 13 06 13" src="https://github.com/user-attachments/assets/0e3bf13a-b441-4e53-908b-8f6eed4bb9f7" />


