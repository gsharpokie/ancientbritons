# Who Were the Ancient Britons?

An animated look at 8,000 years of migration into Britain, built on published ancient-DNA studies. Students start with Cheddar Man, a hunter-gatherer buried about 10,000 years ago, and predict how many times newcomers replaced about half or more of Britain’s ancestry. Then boats cross from the continent, the newcomers become tiles in Britain’s gene pool, and the pool stirs as generations pass. By Gwen Sharp.

**Live site:** https://gsharpokie.github.io/ancientbritons/

## What it does

- **A prediction:** never, once, twice, or three times?
- **The gene pool.** One hundred tiles, each standing for 1% of the ancestry of everyone living in Britain (not 1% of the people). Students step through four moments: hunter-gatherers (about 8000 BCE), the first farmers (about 4000 BCE), Beaker-era newcomers (about 2450 BCE), and Bronze Age newcomers (about 1000 BCE). A running list gives each group’s share at every step. Back, Next arrival, and Replay buttons control the pace.
- **What their DNA shows.** Four bars give the share of tested people in each period who carried gene variants linked to light skin, blue eyes, and digesting milk as adults. A short explainer covers what a gene variant is and what it can’t tell you.
- **The “Bell Beaker” pop-up** shows two public-domain photos of Beaker pots and links to a Natural History Museum article.
- **The reveal,** including the early medieval migration from what’s now Germany and Denmark.
- **What this can’t show,** things to ponder, sources, and accessibility information (closed until opened).

Nothing a student enters is saved or sent anywhere.

## For instructors

- Have students make their prediction individually, then compare in pairs before they watch.
- The “Things to ponder” questions work well for a short written reflection or small-group discussion. The first connects the DNA bars to how racial categories get built; the second asks what else could explain why earlier groups left fewer descendants.
- Link to `https://gsharpokie.github.io/ancientbritons/#crowd` to skip the prediction (for example, on a projector).

## Updating the numbers

Open `index.html` on GitHub, select the pencil icon, and look in the `<script>` section:

- `const STAGES = [` holds the four steps: the date, the place, the caption, the source, and the shares shown in the ancestry list (`show`).
- `const REPLACE = [` sets how many of the 100 tiles change at each arrival, as `[from group, to group, how many]`. If you change the published estimates in `STAGES`, change these to match.
- `const TRAITS = [` holds the four DNA bars for each period (as percentages) and the note with the dates and number of people tested.
- The reveal (including the early medieval figure) is in the line that begins `$("#verdict").innerHTML`. The “What this can’t show” section, things to ponder, and sources are typed into the page text. Update them by hand.

## How the numbers were made

The gene pool follows three published estimates: farmers replaced nearly all earlier ancestry in Britain (Brace et al. 2019); Beaker-era newcomers replaced about 90% (Olalde et al. 2018); and Bronze Age newcomers contributed about half the ancestry of Iron Age England and Wales (Patterson et al. 2022). The page splits the other half between the earlier groups in the same 9-to-1 proportion.

The DNA bars were calculated for this page from the Allen Ancient DNA Resource (AADR), version 66.p1, 1240K data set: people buried in the United Kingdom with a date and a passing quality rating, each counted once. Before publishing, the calculation was checked against published frequencies for the same variants. Each bar counts people who carried at least one copy of the variant, which isn’t the same as the share who had the trait.

## Turning on the site (one time)

Go to **Settings → Pages**. Under **Build and deployment**, set **Source** to **Deploy from a branch**, choose the **main** branch and the **/ (root)** folder, and select **Save**. Keep Issues turned on so the correction and accessibility links work.

## Sources

Brace, Selina, et al. 2019. “Ancient Genomes Indicate Population Replacement in Early Neolithic Britain.” *Nature Ecology & Evolution* 3(5):765–771. Furholt, Martin. 2018. “Massive Migrations? The Impact of Recent aDNA Studies on Our View of Third Millennium Europe.” *European Journal of Archaeology* 21(2):159–191. Gretzinger, Joscha, et al. 2022. “The Anglo-Saxon Migration and the Formation of the Early English Gene Pool.” *Nature* 610(7930):112–119. Heyd, Volker. 2017. “Kossinna’s Smile.” *Antiquity* 91(356):348–359. Mallick, Swapan, et al. 2024. “The Allen Ancient DNA Resource (AADR): A Curated Compendium of Ancient Human Genomes.” *Scientific Data* 11(1):182. Mallick, Swapan and David Reich. 2026. “The Allen Ancient DNA Resource (AADR),” version 66.p1. Harvard Dataverse. Olalde, Iñigo, et al. 2018. “The Beaker Phenomenon and the Genomic Transformation of Northwest Europe.” *Nature* 555(7695):190–196. Patterson, Nick, et al. 2022. “Large-Scale Migration into Britain during the Middle to Late Bronze Age.” *Nature* 601(7894):588–594. Links are on the page.

Photos of Bell Beaker pots (cropped, in `images/`), both released to the public domain (CC0) on Wikimedia Commons: beakers from Thickthorn Down, Dorset, by Pasicles; beaker from Fuente-Olmedo, Spain, by Laci3.

## Accessibility

This site aims to meet [WCAG 2.1](https://www.w3.org/TR/WCAG21/) Level AA, so it works for people who use screen readers, keyboards, or screen magnification.

- All buttons and links can be reached and used with a keyboard, and show a visible outline when selected.
- The gene pool has a text equivalent: the “Ancestry in Britain” list beside it gives each group’s share at every step.
- The DNA bars show their percentages as text.
- The boat animation is skipped for anyone whose device is set to reduce motion.
- The “Bell Beaker” pop-up opens with a click, a tap, the keyboard, or a mouse hover, and closes with Escape. Its photos have text descriptions.
- Each group has its own shape as well as its own color, so color isn’t the only way to tell them apart.
- Text meets WCAG AA color contrast standards in both light and dark mode.
- The page fits narrow phone screens without sideways scrolling.

I checked it in November 2026 with automated accessibility testing (axe-core) plus keyboard and small-screen checks. It hasn’t yet been tested by people who use screen readers every day, so there may be problems I haven’t caught. If something doesn’t work for you, please [let me know](https://github.com/gsharpokie/ancientbritons/issues/new).

The same information is on the page itself, under **Accessibility information** at the bottom.

## Author

Created by Gwen Sharp ([@gsharpokie](https://x.com/gsharpokie)).

## License

© 2026 Gwen Sharp. Licensed under [CC BY-NC 4.0](https://creativecommons.org/licenses/by-nc/4.0/): you may share and adapt it for noncommercial purposes with credit. See [LICENSE](LICENSE).
