# Bildterapihuset Redesign, wu1  | Post Mortem 

Alexander Donev Heino, TE20 - 2022-03-10

## Inledning
Målet med denna uppgift var att skapa en hemsida för Bildterapihuset i kollaboration med Digitalt Skapande. Under DS så skapade vi en redesign för en redan etablerad sida och utvecklade en figma-skiss ifrån detta. I Webbutvecklingens delen använder man denna skiss och kodar fram den med hjälp av HTML och CSS.

## Bakgrund
De inledande processerna hände främst på Digitalt Skapande. I grund och botten visste vi inte att dessa skulle utvecklas som hemsidor vid ett senare tillfälle men nu är vi här ändå. Under idé-tillfällena började vi med att analysera Bildterapihusets nuvarande hemsida (vad jag vet används den dock inte längre). Denna analys syftade på alla olika plus och minus vi kunde hitta på hemsidan. Detta kunde variera mellan navigations svårigheter, tråkig layout, gömda knappar och länkar, mm. Med hjälp av detta blev det lättare att utveckla sin skiss eftersom man visste redan var problemen låg i detta tillfälle. Fortsättningsvist gjorde vi en "User research" och skapade en målgrupp för hemsidan. Här kunde man ganska lätt argumentera att användarna av hemsidan var åt det gammlare hållet, och därför bör den anpassas för det. Hädanefter hoppade vi in i skapandet av grunden till skissen med hjälp av både Information Architecture samt Wireframing. Med dessa två hade vi en grundläggande upplaga för hur hemsidan skulle fungera, alltså UX. Dock var UI inte riktigt uttänkt än. 

Däremot, med det sagt var det nästa del av processen. Första skapade vi Mood Boards och refererade till bilder, typsnitt och design-principer för våran Figma-skiss.
![Moodboard](/assets/images/moodboard.png)

Ifrån detta började man utveckla skissen på hemsidan som sedan skulle användas för Webbutvecklingen.

Desktop design: https://www.figma.com/file/Zos15xDTwKv20a0qFNzuIW/Bildterapi-Desktop-Design?node-id=0%3A1

Mobile design: https://www.figma.com/file/nKld5Dz0TOznolb9NH8JgR/Bildterapi-Design?node-id=0%3A1

Mer om detta kan du hitta i Digitalt Skapande uppgiften: https://docs.google.com/document/d/1UJRKX75YItQMYA9wgi6VAfT-4DmiljcYiY5TxZ3nzmc/edit?usp=sharing

Ifall länken inte är delad kan du kolla på en klon av dokumentet här: https://docs.google.com/document/d/1xGAx6PmiymIUYF0vvLKPMCyeqd1N9nfyeD7AznIJf1g/edit?usp=sharing

Några veckor eller så efter att Digitalt Skapande uppgiften var avklarad skulle vi börja på att utveckla den som en riktig hemsida på Webbutvecklingen. Med tanke på att hela idé-skapande processen samt skissande var helt klart till att börja med kunde man hoppa in i projektet direkt utan några större problem. Med hjälp utav Visual Studio Code kodade jag framm hemsidan med alla olika taggar, attribut och stilar. Detta blev faktiskt den längsta delen i total tid. Vi har redan använt oss utav de grundläggande koncepten inom webbutveckling sedan tidigare, så denna front var inget ut ur det ovanliga. 

Jag började med att skapa Landing Page, den allra viktigaste sidan eftersom det inte minst är detta första intrycket på sidan men mycket man skapar på första sidan kan återanvändas på resten av sidorna. Detta kan vara allt mellan header (som följer med in princip överallt), uniforma knappar och containerns som fungerar på liknande sätt. Därför var denna sida det som tog längst tid utav alla. Dock var första steget att få upp en struktur och bry mig om CSS senare. Navbar, bildplaceringar, text och rubriker kom först. När jag hade placerat allting som planerat i index.html kunde jag finslipa alla delar med själv av style i CSS. Det var även CSS som används för att placera allting på rätt plats, osv.

När allt detta var klart kom det fram till finslipningsmomentet. Vissa bilder behövde anpassa sig positions-mässigt, vilket skapande en hel rad av problem. Men min lösning funkade eventuellt (se lösningen för "abstract_paint.jpg" i index.html och css). Efter detta kom en stor vägg som jag skulle vilja kalla för headern. Det blev en hel rad av saker som behövde fixas, eftersom i ena sekunden hade jag en preliminär header som funkade perfekt. Men när jag i tur och ordning stoppade in en enstaka sak föll allting ihop. I detta fall var det loggan i vänster som pajade allting. Det tog en ganska bra stund att fixa, men med hjälp av Stack Overflow och lite eget tänkande kom jag fram med en lösning som gjorde att listan hamnade på rätt plats även om loggan var del av headern.

Sedan fick vi lära oss om ett nytt koncept i form utav Media Queries. Med detta kan man modifiera hur och när hemsidan ska förändras beroende på storleken av fönstret. Jag var tyvärr sjuk under detta moment och behövde jaga efter lite granna. På grund av detta finns det inte heller någon etablerad mobilversion, men grunden till den finns där. Iallafall går det att ändra storleken på desktop versionen.

Jag påbörjade någonting nytt som jag aldrig har testat förr, men hann inte riktigt klart med det. Detta är implementationen av Google Maps på sidan. Man kan hitta ett försök av detta i kontaktadress.html men när jag försökte plugga fram ett fungerande API kände jag att det blev lite för komplicerat samt tidsbedrivande. Kartan är tekniskt sätt där men den fungerar ej.

När allting in princip var klart kunde jag använda Wave för att hitta några visuella och lätthanterbara problem och sedan validera med hjälp av diverse hemsidor för att hitta kod-snuttar som var fundamentalt fel. I Wave fanns det faktiskt inte mycket problem, endast Date input typen som saknade en legitim label tagg runtom den. Här fastnade jag faktiskt eftersom jag inte använt input förr och varje label jag försökte implementera. Detta problem kvarstår alltså. Validering hade några "children" problem, dock fixade jag de flesta. Det kvarstår endast en nu som jag inte heller riktigt förstår eller har tid för. Det får inte finnas en div innuti en ul men den är en ganska stor del av det fundamentala i uppbygget av min navbar. Det är helt enkelt någonting jag får tänka på tills nästa gång.

## Positiva erfarenheter
I sin helhet hade jag väldigt kul med även denna uppgift. HTML och CSS är saker jag kan förstå och på så sätt kan jag utveckla utan dessvärre problem. Jag blev väldigt nöjd med slutprodukten och om man jämför den med skissen är den väldigt lik målet. In princip alla problem jag halkade på löste jag eventuellt, vilket känns bra eftersom jag förstår i grund och botten vad som behöver lösas.

## Negativa erfarenheter
På samma gång var mina negativa erfarenheter absolut de tillfällena där jag fastnade längre än vad jag borde. Med det sagt tappade jag säkert mycket tid på småjusteringar som egentligen inte gjorde så stor skillnad. Däremot kunde jag verifiera att allting faktiskt fungerade. Men av just denna anledning kunde jag inte finalisera vissa delar av projektet som mobil-versionen, kartan samt alla sidor. Väl vid valideringen hittade jag några problem som var lite ur mina händer. När man väl validerar har man kommit så långt på vägen, men det fanns ett visst fel den poängterade som jag skulle behövt hjälp på. Den säger att vissa taggar "inte får" vara en "child" av en annan. Men ifall jag hade försökt problemlösa detta skulle mycket av strukturen helt enkelt falla ihop. Den som kom fram mest var att länkar inte får "krama" knappar, men för att hela knappen faktiskt ska ta mig någonstans och inte bara t.ex. texten behövde jag placera länken där. 

## Sammanfattning
Jag har skapat en hemsida för min redesign av Bildterapihuset. Som vanligt hade jag kul med uppgiften och skapade en produkt som inte bara var lik skissen, men jag var även mycket nöjd med den. Det finns än några förbättrings fronter, så som att kolla in djupare på API och skapandet av kartor, jQueries, mobilanpassning och några strukturproblem (upptaget i negativa erfarenheter).

