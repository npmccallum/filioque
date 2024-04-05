This is a repository collecting information on the Filioque. Its goal is to paint an accurate picture of the development with a focus on a reevaluation of the conflict in objective terms unshaped by the apologetics of each side.

Here is the legend for the graph below.

```mermaid
graph TB
    subgraph Shapes
        council[("Council    ..")]
        imperial{{"Imperial Edict    ..."}}
        baptismal(["Baptismal Creed    ..."])
        consensus[/"Consensus Creed    ..."\]
        eucharistic[["Eucharistic Creed    ..."]]
        miscellaneous("Miscellaneous    ...")
        style council fill:#00000000
        style imperial fill:#00000000
        style baptismal fill:#00000000
        style consensus fill:#00000000
        style eucharistic fill:#00000000
        style miscellaneous fill:#00000000
    end

    subgraph Colors
        basic["'the Holy Spirit'  ..."]
        extra["additional HS statements  ....."]
        proceeds["'who proceeds from the Father...'  ......."]
        receives["'... and receives from the Son'  ......"]
        through["'... through the Son'  ...."]
        filioque["'... and the Son'  ..."]
        style basic fill:#FFFF00
        style extra fill:#CCF533
        style proceeds fill:#99EB66
        style receives fill:#66E099
        style through fill:#33D6CC
        style filioque fill:#00CCFF
    end
```

And here is a graph detailing the relationships between statements about the Holy Spirit in creeds.

```mermaid
graph TB
    edict{{"==== Edict of Thessalonica (380) ===="}}
    edict ~~~ constantinople
    epiphaniusb ~~~ edict

    subgraph Greek
        marcellus(["Marcellus (~340)    ..."])
        style marcellus fill:#FFFF00

        deirbalyzeh(["Deir Balyzeh (~350)    ..."])
        style deirbalyzeh fill:#FFFF00

        marcellus ~~~ deirbalyzeh ~~~ marcellus

        jerusalem(["Jerusalem (~350)    ..."])
        style jerusalem fill:#CCF533
        
        nicea[("Nicea (325)    ...")]
        constantinople[("Constantinople? (381) ....")]
        ephesus[("Ephesus (431)    ...")]
        chalcedon[("Chalcedon (451)    ...")]
        style nicea stroke-dasharray:3
        style constantinople stroke-dasharray:3
        style nicea fill:#FFFF00
        style constantinople fill:#99EB66
        style chalcedon fill:#99EB66
        style antiochian fill:#99EB66
        style byzantine fill:#99EB66

        nestorius["Nestorius (430)    ..."]
        eusebius[/"Eusebius    .."\]
        athanasius[/"Athanasius    ."\]
        basil[/"Basil    ."\]
        epiphaniusa[/"Epiphanius A (374)    ..."\]
        epiphaniusb[/"Epiphanius B (374)    ..."\]
        style nestorius fill:#FFFF00
        style eusebius fill:#FFFF00
        style basil fill:#FFFF00
        style athanasius fill:#FFFF00

        style epiphaniusa fill:#99EB66
        style epiphaniusb fill:#66E099

        antiochian[["Antioch (~475)    ..."]]
        byzantine[["Byzantine Rite (6th c.)    ..."]]

        marcellus -.-> eusebius
        marcellus -.-> jerusalem
        eusebius --> nicea
        jerusalem ~~~ nicea

        nicea --> basil
        nicea --> nestorius
        nicea --> athanasius
        nicea --> epiphaniusa

        jerusalem --> epiphaniusa

        epiphaniusa --> epiphaniusb
        epiphaniusa --> constantinople

        constantinople --> chalcedon
        constantinople --> antiochian
        constantinople --> byzantine

        nestorius ~~~ ephesus

        ephesus ~~~ chalcedon
        chalcedon ~~~ antiochian
        constantinople ~~~ ephesus
        constantinople ~~~ nestorius
    end

    subgraph Armenian
        armenian(["Armenian (~425)    ..."])
        armenia[["Armenia (unk.)    ..."]]
        style armenian fill:#99EB66
        style armenia fill:#99EB66
        armenian --> armenia
    end

    subgraph Latin
        oldroman(["Old Roman (~150)    ..."])
        damasus[/"Damasus (382-447)    ..."\]
        leo("Leo Epistle 15 (447)    ...")
        apostles(["Apostles' (~450)    ..."])
        toledoa[/"Toledo I (400)    ..."\]
        toledob[/"Toledo II (447)    ..."\]
        toledoc[/"Toledo III (589)    ..."\]
        athanasian[/"Athanasian (5th c.)    ..."\]

        spain[["Spain (6th c.)"]]
        gallican[["Gallican Rite? (7th c.)"]]
        frankia[["Frankia (8th-9th c.)"]]
        hre[["Holy Roman Empire (10th c.)"]]
        rome[["Rome (11th c.)"]]

        style oldroman fill:#FFFF00
        style apostles fill:#FFFF00
        style damasus fill:#00CCFF
        style leo fill:#00CCFF
        style toledoa fill:#99EB66
        style toledob fill:#00CCFF
        style toledoc fill:#00CCFF
        style athanasian fill:#00CCFF
        style spain fill:#00CCFF
        style gallican fill:#00CCFF
        style athanasian fill:#00CCFF
        style frankia fill:#00CCFF
        style hre fill:#00CCFF
        style rome fill:#00CCFF
        
        oldroman --> apostles
        athanasian ~~~ toledoc

        toledoa --> toledob
        toledob -. "and the son .." .-> toledoc
        toledoc --> spain

        damasus --> leo
        leo -. "homoousias ... and the son ......" .-> toledob
        oldroman ~~~ nicea

        spain --> gallican
        gallican --> frankia
        frankia --> hre
        hre --> rome
    end

    oldroman --> marcellus


    epiphaniusb -. "Jerome? .." .-> damasus

    constantinople --> armenian
    damasus ~~~ constantinople ~~~ damasus
    chalcedon --> toledoc

    antiochian ~~~ byzantine
    antiochian ~~~ spain

    toledoc ~~~ armenia
    armenian ~~~ nestorius
```
