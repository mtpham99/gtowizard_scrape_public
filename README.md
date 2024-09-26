# GTOWizard Ranges Webscraper

Webscraper written in Python for scraping ranges from the [GTOWizard](https://app.gtowizard.com/solutions) app.

The code for the webscraper is not public, but the scraped ranges are available for download [here](https://github.com/mtpham99/gtowizard_scrape_public/releases/tag/v0.1-ranges-only).

If you have any questions, send an email to [gtowizard-scraper-help@quantamail.net](mailto:gtowizard-scraper-help@quantamail.net).


# Table of Contents

1. [Format](#1-format)
2. [Available Ranges](#2-available-ranges)
3. [GTO+ / Flopzilla Instructions](#3-gto--flopzilla-instructions)
4. [Feedback / FAQs](#4-feedback--faqs)


## 1. Format

### 1.1 Zip File Name

Ranges are saved and zipped into a file named using the GTOWizard solution parameters used to scrape the ranges. For example, `cash6m_100bb_nl500_25open_small3bet.zip` corresponds to:

- solution type: cash
- players: 6
- stack: 100
- rake: nl500
- opening size: 2.5x
- 3bet size: smaller

Each zip file contains a `info.txt` file with more detailed parameters.


### 1.2 Directory Structure

Inside each unzipped folder, the ranges are stored under the `ranges` folder.

Ranges are saved under a directory structured to reflect the preflop actions. For example, `ranges/UTG/2bb/BB/12bb/UTG/call/UTG.txt` is the text file containing UTG's range when UTG opens with 2bb, action folds to BB, BB 3-bets to 12bb, and UTG calls. Similarly, `ranges/UTG/2bb/BB/12bb/UTG/call/BB.txt` contains BB's 3-bet range in the same preflop scenario.


### 1.3 Range File Format

Each range text file (e.g., `ranges/UTG/2bb/BB/12bb/UTG/call/UTG.txt`) contains one line. This line contains each hand (pair/suited/offsuit) and its probability separated by a colon. Each hand/probability pair is separated by a comma. For example: `AA:1.0,AKs:1.0,AQs:1.0,...,AKo:0.0,KK:1.0,AQo:0.0,...`.

This format is compatible with [GTO+](https://gtoplus.com) and [Flopzilla](https://flopzilla.com). If you need the ranges in a different format, email a request to [gtowizard-scraper-help@quantamail.net](mailto:gtowizard-scraper-help@quantamail.net).


## 2. Available Ranges

I will scrape a handful of common/frequently requested ranges and make them available [here](https://github.com/mtpham99/gtowizard_scrape_public/releases/tag/v0.1-ranges-only). The common/frequently requested ranges are listed below. The ranges without a checkmark are still in-progress of being scraped.

If the ranges you'd like scraped are not listed below, you can request them by emailing [gtowizard-scraper-help@quantamail.net](mailto:gtowizard-scraper-help@quantamail.net). If enough people are interested, I will add it to the list.

Scraped Ranges Progress:

- [x] `cash6m_50bb_nl50_gto_gto`
    - solutions: cash
    - type: classic
    - players: 6max
    - available spots: postflop included
    - stacks: 50
    - bet sizes: general
    - rake: nl50
    - opening size: gto
    - 3bet size: gto
- [x] `cash6m_100bb_nl50_gto_gto`
    - solutions: cash
    - type: classic
    - players: 6max
    - available spots: postflop included
    - stacks: 100
    - bet sizes: general
    - rake: nl50
    - opening size: gto
    - 3bet size: gto
- [x] `cash6m_200bb_nl50_gto_gto`
    - solutions: cash
    - type: classic
    - players: 6max
    - available spots: postflop included
    - stacks: 200
    - bet sizes: general
    - rake: nl50
    - opening size: gto
    - 3bet size: gto
- [x] `mttchipev8m_25bb_withlimps`
    - solutions: mtt
    - format: chipev
    - players: 8
    - available spots: postflop included
    - effective stack: 25
    - variant: with limps
- [ ] `mttchipev8m_50bb_withlimps`
    - solutions: mtt
    - format: chipev
    - players: 8
    - available spots: postflop included
    - effective stack: 50
    - variant: with limps
- [ ] `mttchipev8m_80bb_withlimps`
    - solutions: mtt
    - format: chipev
    - players: 8
    - available spots: postflop included
    - effective stack: 80
    - variant: with limps


## 3. GTO+ / Flopzilla Instructions

*Note the steps are identical for GTO+ and Flopzilla*

1. Download a zip file of ranges from [here](https://github.com/mtpham99/gtowizard_scrape_public/releases/tag/v0.1-ranges-only)
2. Unzip the downloaded ranges zip file
3. Goto the `Settings` menu in GTO+/Flopzilla
4. Click on `Import predef ranges from newdefs2.txt or newdefs3.txt`
5. Toggle the first option to select `pio/monker/other`
6. Toggle the second option to select `Import into sub-category`
7. Click on `Import Ranges` and select the folder inside the unzipped ranges folder from `step 2`
8. Wait
9. Ranges should be visible under "Imported Ranges"


## 4. Feedback / FAQs

If you have any questions or feedback, send an email to [gtowizard-scraper-help@quantamail.net](mailto:gtowizard-scraper-help@quantamail.net).


### 4.1 Missing Ranges / Preflop Scenarios

If there are any ranges missing, double check that the preflop scenario is available on [GTOWizard](https://app.gtowizard.com/solutions). If the preflop scenario is available on [GTOWizard](https://app.gtowizard.com/solutions) but missing from the scraped ranges, send an email to [gtowizard-scraper-help@quantamail.net](mailto:gtowizard-scraper-help@quantamail.net) detailing the missing scenario.

The scraping process involves generating desired preflop scenarios, then scraping the associated ranges rather than scraping available preflop scenarios directly from [GTOWizard](https://app.gtowizard.com/solutions). The preflop scenario generation process is automated to generate specific scenarios based on a filter. Therefore, some uncommon (or accidentally missed) scenarios may have been (accidentally) filtered out.


### 4.2 Range / Solution Settings Not Available

If the ranges you are looking for are not in the [list above](#2-available-ranges), you can request them by emailing [gtowizard-scraper-help@quantamail.net](mailto:gtowizard-scraper-help@quantamail.net) with a screenshot of the settings from [GTOWizard](https://app.gtowizard.com/solutions) or specifying the settings like the [list above](#2-available-ranges). If enough people request the same settings, I will add them to the list.


### 4.3 Postflop Ranges

I do not plan to scrape postflop ranges.
