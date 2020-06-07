---
layout: post
title: "Kritische Notizen zur Blockchain"
date: 2018-01-07
teaser-img: 2018-01-07-teaser.png
---

Eigentlich sollte der folgende Text [in meinem Newsletter erscheinen][1]. Jedoch wurde er schnell deutlich zu lang für eine E-Mail, weswegen ich mich entschlossen habe ihn hier zu veröffentlichen. Ich versuche normalerweise in meinem Newsletter einigermaßen regelmäßig über Technologien zu schreiben und ihre Auswirkungen, Entwicklung und Bedeutung einzuordnen. Entsprechend war mein eigentliches Ziel dies auch für die Blockchain zu tun.

Nur hier ist das Problem: Es ist für mich fast unmöglich zu einer klaren Aussage zur Blockchain zu kommen oder eine Einschätzung abzugeben. Je tiefer man in die Materie einsteigt, desto mehr Widersprüche scheinen sich zwischen dem öffentlichen Image von Blockchain und der Realität der Technologie aufzutun.

Dieser Text ist also keine endgültige Einschätzung der Technologie, sondern viel mehr meine Recherche und Notizen ausformuliert. Entsprechend würde ich mich über Anmerkungen und Kommentare freuen.

## Was ist die Blockchain?

Es gibt einige Artikel, die die Funktionsweise einer Blockchain weitaus detaillierter und besser beschreiben können, als ich es hier machen werde. Aber kurz zusammengefasst: Die Blockchain ist das zugrundeliegende Datenbank-Konzept der meisten Kryptowährungen und wurde in seiner grundsätzlichen Form von Satoshi Nakamoto, dem mythischen Erfinder von Bitcoin, beschrieben. Eine Blockchain erlaubt es mehreren Parteien zusammenzuarbeiten, ohne dass diese sich kennen und vertrauen müssen. Ermöglicht wird dies durch ein kryptografisches Verfahren.

Mohit Mamoria hat die Funktionsweise hier auch [sehr detailliert und verständlich noch einmal aufgeschlüsselt][2]. (Danke an [Marie Kilg][3] für den Hinweis 🙌🏻)

Wer es etwas gerne etwas audiovisueller hat, dem sei dieses Video von WIRED ans Herz gelegt:

{% include youtube-embed.html id="https://www.youtube.com/embed/hYip_Vuv8J0" %}

Jedoch muss hier gleich eine Sache im Kopf behalten werden: Auch wenn viel von Blockchain als singuläre Technologie gesprochen wird, umfasst der Begriff tatsächliche eine ganze Reihe unterschiedlicher Technologien, Techniken und Konzepte.

Grundsätzlich muss auch zwischen öffentlichen (oder permissionless) Blockchains und privaten (oder permissioned) Blockchains unterschieden werden. Während in öffentlichen Blockchains jeder Teil des Netzwerks werden kann — wie beispielsweise bei Kryptowährungen — erhalten in privaten Blockchains nur ausgewählte Teilnehmer Zugriff. Die meisten Blockchain-Implementierungen in Banken oder Unternehmen sind beispielsweise private Blockchains.

Ein anderer wichtiger Aspekt, den man im Blick behalten sollte, ist die Tatsache, dass die Blockchain als Konzept selbst auf [einer ganzen Reihe anderer Technologien basiert][4]. Die historische Perspektive ist zwar nicht unbedingt ausschlaggebend, aber dennoch wichtig zu berücksichtigen. Oder wie die Autoren es selbst beschreiben: „Nakamoto’s genius, then, wasn’t any of the individual components of bitcoin, but rather the intricate way in which they fit together to breathe life into the system.“

{% include img-full.html id="2018-01-07-01.png" alt="" info="via Arvind Narayanan und Jeremy Clark"%}

## Hype

Okay, kommen wir zu dem Problem, das die Berichterstattung rund um Blockchain unheimlich schwer einzuschätzen macht: H Y P E !

Artikel rund um die möglichen Auswirkungen der Technologie sind voll von gigantischen Versprechen, überzogenen Erwartungen und einer guten Prise „Magical Thinking“. Und immer wieder trifft man auf Artikel, die verkünden, dass die Blockchain eine beliebige Industrie (meist die Finanzindustrie) „disrupten“ wird. Es wird jedoch in vielen Fällen deutlich, dass Autoren solcher Artikel keinen Schimmer von der Industrie haben, die sie disrupten wollen, und sehr oberflächliche Analysen anstellen. (Allgemein sollten solche breiten Aussagen immer mit viel Vorsicht genossen werden)

Ich weiß auch ehrlich nicht, ob man wirklich von einer „Disruption“ der Finanzindustrie sprechen kann, bei der Geschwindigkeit mit der sie selbst Blockchain-Projekte startet—[und das schon seit mehreren Jahren][5].

Das nächste große Problem ist die Definition des Begriffs „Blockchain“. Dadurch, dass der Begriff eine ganze Reihe an unterschiedlichen — wenngleich sich ähnelnden — Technologien beschreibt, ist er schwer festzunageln. Was derzeit passiert ist, dass sich Firmen und Startups einzelne in der Blockchain verwendete Methoden herauspicken und diese dann als „Blockchain“ verkaufen. So beispielsweise geschehen [im Falle der Estland-Blockchain][6], bei der es sich schlicht [um einen Merkle-Baum handelt][7]. (Eine der grundlegenden historischen Ideen der Blockchain, aber eben nicht eine reine Blockchain)

Diese Verwendung des Begriffs ähnelt [stark der Verwendung von „KI“][8] als schlichtes Marketingkonstrukt. Es befeuert weiter den Hype, macht es aber schwierig die Technologie wirklich einzuschätzen.

## Limits

Eine Methode, die sich für mich in den letzten zwei Jahren bewährt hat, ist bei viel gehypten Technologien nach deren Limitierungen zu suchen. Meist zeichnen diese ein sehr viel deutlicheres Bild über die Möglichkeiten einer Technologie, als beliebige Zukunftsszenarien, die “Was-wäre-wenn?” spielen.

Ein guter Einstiegspunkt hierfür ist Preethi Kasireddys Artikel, [der gut die derzeitigen technischen Probleme der Technologie zusammenfasst][9] und auch Lösungsansätze liefert. Zwar bezieht sich ihr Text hauptsächlich auf öffentliche Blockchains, jedoch dürften die technischen Limitierungen auch auf private zutreffen. (Es lohnt sich auch den Text zu lesen, wenn man sich tiefer mit der Materie beschäftigen will.)

Zusammengefasst steht die Blockchain-Technologie vor den folgenden technischen Hürden:

- **Limited scalability** — Die dezentralisierte Natur einer Blockchain führt derzeit zu begrenzten Transaktionen pro Sekunde und dadurch einer langsamen Transaktionszeit.
- **Limited privacy** — Öffentliche Blockchains sind by design von jedem im Netzwerk einsehbar. (Tschüss, Bankgeheimnis…)
- **Lack of formal contract verification **— Smart Contracts sind eine schöne Idee, in der Praxis jedoch oft unsicher und angreifbar.
- **Storage constraints** — Die dezentralisierte Natur einer Blockchain führt dazu, dass jede Node im Netzwerk die volle Datenbank abspeichern muss, was Speicheraufwendig werden kann.
- **Unsustainable consensus mechanisms** — So viele Probleme: Energieverschwendung, um die Blockchain weiter zu schreiben, und Machtgefälle innerhalb des Netzwerkes, die für dieses gefährlich werden könnten.
- **Lack of governance and standards **— Dezentralisierung ist gut und schön, bis sich alle auf Updates und Patches einigen müssen.
- **Inadequate tooling** — Blockchain-Technologie ist verdammt komplex und schwer zu verstehen, selbst für erfahrene Entwickler.
- **Quantum computing threat** — Eher theoretisch: Quantencomputer könnten die Verschlüsselung einer Blockchain knacken und sie so über Nacht vollkommen nutzlos machen.

Und auch hier treffen wir wieder auf das Problem, dass der Begriff „Blockchain“ eine ganze Reihe an Technologien umfasst, die unterschiedlich anfällig für die oben aufgeführten Probleme sind. Es ist unheimlich kompliziert in diesem Feld auch nur ansatzweise durchzusteigen.

Bei privaten Blockchains kommt noch ein zusätzlicher Faktor ins Spiel. Eine Blockchain-Datenbank dürfte für 99% dieser Anwendungsfälle totaler Overkill sein. [Oder wie Arvind Narayanan es beschreibt][10]: 

> To build these private blockchains, banks start with the Bitcoin Core code and rip out all the parts they don’t need. It’s a bit like hammering in a thumb tack, but if a hammer is readily available and no one’s told you that thumb tacks can be pushed in by hand, there’s nothing particularly wrong with it.

Das alles bringt uns zu der Frage: Brauche ich überhaupt eine Blockchain für mein Problem? Karl Wüst und Arthur Gervais von der ETH Zürich haben versucht genau diese Frage in ihrer Studie „[Do you need a Blockchain?][11]“ zu beantworten. Ihr Ergebnis: Vermutlich eher nicht. Zwar gäbe es durchaus valide Use-Cases in Bereichen, wie im Supply/Demand-Chain-Managment, Banking, Proof-of-Ownership oder E-Voting, aber all diese Use-Cases kommen mit Einschränkungen daher. Wüst und Gervais haben ihre Ergebnisse auch in einem praktischen Flow-Chart zusammengefasst.

{% include img-full.html id="2018-01-07-02.jpg" alt="" info="via Arvind Narayanan und Jeremy Clark"%}

Jedoch sollten auch Use-Cases wie Banking oder E-Voting mit Vorsicht genossen werden. SaveOnSend, ein Startup, welches sich auf internationale Geldüberweisungen spezialisiert, hat in einem langen Blog-Post die Versprechen von Bitcion/Blockchain [als Banking- und Überweisungssystem in Schwellen- und Entwicklungsländern auseinandergenommen][12]. Auch hier zeigt sich wieder das Problem, dass viele Blockchain-Evangelisten wenig bis gar keinen Einblick in die Industrie haben, die sie „disrupten“ wollen.

Und der Entwickler Ben Adida hat einen ebenfalls kritischen Artikel [über den Einsatz von Blockchain bei Wahlen geschrieben][13]. 

> Blockchain can help a bit with voting, but it’s not doing the most important part of the work. It doesn’t help tally secret ballots in a publicly verifiable way. It doesn’t provide individual verifiability that a ballot was correctly encoded. And it’s not useful for voting eligibility, since that’s all about human authentication and a centrally produced voter list. At best, in voting, Blockchain can be a ledger that helps us track the voting metadata.

(Ich gehe auch fest davon aus, dass wir in den nächsten Wochen und Monaten vermehrt kritische Artikel zu anderen Use-Cases sehen werden.)

Und hier kommen wir abschließend wieder zu der historischen Perspektive der Blockchain. Es ist jetzt 10 Jahre her, dass die Blockchain existiert, und es hat bisher noch niemand einen echten Use-Case außerhalb von Kryptowährungen [oder Nischen gefunden, argumentiert Kai Stinchcombe][14].

> In conversations with bitcoin entrepreneurs and investors and consultants, there was often a lack of knowledge or even interest in how the jobs were being done today or what the value to the end user was. With all the money spent on bitcoin cash registers, nobody went out and did a survey about whether most credit card users would be willing to give up their frequent flyer miles in return for also losing the ability to dispute a transaction. Presumably, they thought, the reason IPOs are so expensive or venture fund formation paperwork is so onerous is because all those lawyers and accountants are just getting rich sitting around pushing paper… a bunch of smart engineers in their 20s with no industry experience could certainly do their jobs, automatically, in a matter of months, with just a few million bucks of venture capital.

## Fazit

Also, was bedeutet das alles?

Ehrlich, ich habe keine Ahnung. Ich sehe durchaus, warum die Technologie selbst interessant ist, aber aus meiner — zugegeben eingeschränkten — Perspektive überschatten die Nachteile die Vorteile deutlich. Vielleicht werden diese Probleme in neuen Implementierungen der Technologie behoben, vielleicht auch nicht. Feststeht, die Blockchain ist eine fürchterlich über-hypte Technologie, nicht zuletzt getrieben durch den Hype rund um Kryptowährungen und geschickten Marketingabteilungen. Denn eine Blockchain ist scheint letztendlich das zu sein, was man daraus macht.

Wird die Blockchain also die revolutionäre Technologie und der Paradigmenwechsel sein, für die sie viele zu halten scheinen? Zweifellos wird sie in den nächsten Jahren eine große Rollen spielen, ich neige aber dazu „nein“ zu sagen. Es ist aber auch nicht unwahrscheinlich, dass ich mit dieser Einschätzung falsch liege.

Ich denke wir werden es sehen. [Oder aber, um es mit den Worten meines Kollegen Dirk von Gehlen zu sagen][15]: ¯ \ \_(ツ)_/¯.

---- 
## Abschließende Anmerkung: Ideologie und Community

Es gibt schließlich noch zwei letzte Punkte, auf die ich eingehen möchte, die aber eher indirekt mit der Technologie selbst zusammenhängen.

Genauer geht es um Teile der Blockchain-Community, welche große Überschneidungen mit der Community um Kryptowährungen hat. Wer diese länger auf Twitter, in Foren oder auf Reddit beobachtet wird schnell feststellen, dass einige Teile dieser schlicht toxisch sind und bewusst Filterblasen um sich bilden, die die immer gleichen Ideen ständig wiederholen und Kritik ausgrenzen.

Dies äußert sich auch oft in der Reaktion auf kritische Texte mit dem schlichten Hinweis, dass dieser „FUD“ ([Fear, Uncertainty and Doubt][16]) sei. FUD selbst bezeichnet eine Kommunikationsstragie, mit der Furcht, Ungewissheit und Zweifel beim Ziel hervorgerufen werden sollen, im Falle der Community mit dem Ziel Kryptowährungen für Nutzer uninteressant zu machen. Oft tauchen diese Vorwürfe mit der Implikation auf, dass es eine Verschwörung von großen Banken und Unternehmen gäbe, Kryptowährungen zu unterdrücken. „FUD“ ähnelt dadurch in seiner Verwendung stark dem Begriff „Fake News“.

Ein weiterer Aspekt ist die Verwendung von „Nocoiner“ für Kritiker, die selbst nicht in Bitcoin oder andere Kryptowährungen investiert haben. Im Urban Dictionary ist [dieser Begriff wie folgt definiert][17]: (Hervohebungen von mir)

> A Nocoiner is a person who has no Bitcoin. Nocoiners (usually Socialists, Lawyers or MBA Economists ) are people who missed their opportunity to buy Bitcoin at a low price because they thought it was a scam, and who is now bitter at having missed out. The nocoiner takes out his or her bitterness on Bitcoin Hodlers, by constantly claiming that Bitcoin will crash, is a scam, is a bubble, or other types of easily refuted FUD. Nocoiners have little to no computer skills or imagination; even when they see the price of Bitcoin go up and its adoption spread they consider all Bitcoin users to be in a collective delusion, with only themselves as the ones who can see what is happening. **This attitude comes from being steeped in the elitist priest cultures found at Harvard, Yale and Columbia, where anyone who is not part of their clique is treated with suspicion by default. The worst nocoiners are tenured academics and goldbugs. Nocoiners believe that the world owes them everything they want because they are part of an elite**; they are hysterical liars, brats, prostitutes and losers.

Auch wenn diese Definition keineswegs allgemeingültig ist, ist sie jedoch bemerkenswert. Der Fokus auf „Eliten“ als Gegenspieler und die Verwendung von „FUD“ als „Fake News“-Äquivalent ist keine Überraschung, wenn man die Ideologischen Grundlagen von Bitcoin betrachtet. Satoshi Nakamotos ursprüngliches Paper beschreibt [eine stark libertäre Weltsicht][18], auch bedingt durch die Finanzkrise 2007. Die bereits hier formulierten libertären Argumente für Bitcoin ziehen sich noch immer durch die Community und zeigen sich immer wieder anhand der oft sehr breiten Kritik an Zentralbanken, Steuern und allgemeinen Reglementierungen durch Staaten.

David Golumbia, Professor an der Virginia Commonwealth University, hat diese Punkte auch in seinem 2016 erschienen Buch The Politics of Bitcoin: Software as Right-Wing Extremism aufgefasst. Gegenüber dem Blog der Universität[ fasste er seine Kritik wie folgt zusammen][19]:

> The world of Bitcoin bluntly says “government is evil” and “central banking is evil” and “‘we’ can take control back from these institutions with distributed software,” but discourages adherents from investigating how governments function, what central banks do, or even what it means for a nebulous “us” to “take control” away from “centralized institutions,” since in practice this usually means just giving more control to institutions that are less accountable and less transparent than governments.

Auch wenn seine Kritik sich hauptsächlich auf Teile der Bitcoin Community bezieht, sollte die ideologische Motivation einiger Blockchain/Bitcoin-Evangelisten nicht ignoriert werden, [gerade dann wenn Blockchain der Grundstock für eine neue Gesellschaftsordnung sein soll][20].

Es ist eine bequeme Illusion zu glauben, dass Technologie neutral oder aus sich heraus „gut“ ist. Kryptowährungen könnten genauso gut das Einfalltor für eine neue Form technisch ermöglichten Autoritarismus sein, [argumentiert Ian Bogost][21].

> Future cryptocurrencies operated by banks or governments might enjoy more productive use than Bitcoin. But those futures also undermine cryptocurrency’s [anrcho-capitalistic] aspirations. Corporations and governments re-centralize control, for one. But also, they undermine the discretion and anonymity that accompanies free trade in the [anrcho-capitalistic] fantasy. When the local or central bank manages the cryptocurrency platform, it also gets a record of every transaction that takes place in that economy. One doesn’t need to be an anarchist to surmise potential downsides of that situation. Picture China mandating state cryptocurrency, tying the country’s proposed social credit system to that ledger. Or imagine if the North Carolina State legislature decided to issue all food stamp vouchers in crypto form to better manage their future use.

Wir sollten deutlich wachsamer sein, wenn es um den Hype angeblicher neuer technologischer Paradigmen geht, und stärker die Motivationen hinter diesen Technologien hinterfragen. Des einen Utopie wird ansonsten schnell des anderen Dystopie.

[1]:	https://www.getrevue.co/profile/klingebeil
[2]:	https://www.linkedin.com/pulse/blockchain-absolute-beginners-mohit-mamoria/
[3]:	https://twitter.com/mkilg_
[4]:	http://queue.acm.org/detail.cfm?id=3136559
[5]:	https://www.reuters.com/article/us-banks-blockchain/nine-of-worlds-biggest-banks-join-to-form-blockchain-partnership-idUSKCN0RF24M20150915
[6]:	https://www.newyorker.com/magazine/2017/12/18/estonia-the-digital-republic
[7]:	https://davidgerard.co.uk/blockchain/2017/09/06/estonias-smartcard-security-problem-is-probably-not-blockchain-related-but-what-is-estonias-blockchain/
[8]:	https://www.getrevue.co/profile/klingebeil/issues/der-ki-hype-kopierstrategien-und-anchor-47361
[9]:	https://medium.com/@preethikasireddy/fundamental-challenges-with-public-blockchains-253c800e9428
[10]:	https://freedom-to-tinker.com/2015/09/18/private-blockchain-is-just-a-confusing-name-for-a-shared-database/
[11]:	https://eprint.iacr.org/2017/375.pdf
[12]:	https://www.saveonsend.com/blog/bitcoin-blockchain-money-transfer/
[13]:	https://benlog.com/about/
[14]:	https://hackernoon.com/ten-years-in-nobody-has-come-up-with-a-use-case-for-blockchain-ee98c180100
[15]:	http://mediathek.rbb-online.de/tv/zibb/Autor-Dirk-von-Gehlen/rbb-Fernsehen/Video?bcastId=3822084&documentId=48879152
[16]:	https://de.wikipedia.org/wiki/Fear,_Uncertainty_and_Doubt
[17]:	https://www.urbandictionary.com/define.php?term=nocoiner
[18]:	http://www.nytimes.com/2013/12/15/sunday-review/the-bitcoin-ideology.html
[19]:	https://news.vcu.edu/article/VCU_professor_discusses_The_Politics_of_Bitcoin_Software_as_RightWing
[20]:	https://www.ribbonfarm.com/2017/10/10/the-blockchain-man/
[21]:	https://www.theatlantic.com/technology/archive/2017/05/blockchain-of-command/528543/