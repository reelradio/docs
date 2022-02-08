# ReelRadio

## Team

Team Cloud Prime

Team Members:
- Zed Chance
- Victor Galbraith
- Nick Fairneny
- Emmanuel Castrejon
- Kobe Charles
- Cesar Arroyo

Client:
- Professor Barry Brown – Sierra College
- ReelRadio, Inc.

Advising Professor:
- Dr. Ahmed Salem

## Background

ReelRadio is a non-profit dedicated to archiving and hosting “Top 40” radio broadcasts from the 50s thru 80s. Started in the 1990s, ReelRadio is a subscription based service that allows fans to stream old radio broadcasts.

## Scope

The current state of the site is old and broken. The client would like the entire site migrated to a new server. Once on a new server, a new database management system can be swapped in place. This entire migration process will need risk assessment because the site is live with paying subscribers. The migration will involve updating old queries, using modern syntax.

Once this migration is in place, new features can be added. The payment system can be fixed. A new persistent audio player can be added. The site’s search functionality can be greatly expanded, both by searching all the text on the site and analyzing the recordings via voice recognition.

## Proposed Solution

The site needs a lot of upgrades and changes to get to a state that the client wants, but still wants to maintain the same functionality and look as before.

### Migration

The highest priority task is migrating the site to an upgraded server. This will require downtime, and assessing and fixing any broken links and functionality caused by the migration. Once the migration occurs, the server can be put under Git version control, since the old server did not support such functionality. Additionally, we need to migrate the database from MySQL to PostgreSQL, which will require additional time.

### Refactors

The client also needs us to refactor old database queries to match the updated database. This process may take a long time as most of the 1000+ pages are individually coded.

## Highlights

In addition to the fixes we will be implementing the following additional features.

### Expanded search functionality

The site features 100s of biographies and DJ descriptions. Currently, the search feature of the site does not search this text. After migrating the site and database, it would be possible to implement a better in-site search engine. We plan to include searching by date, DJ, and keywords in the description.

### Better audio listening experience

The client also requires us to implement a persistent audio player so that users can listen to the recordings while browsing the site. This is meant to replace the current method of listening, which requires users to download the recordings and listen through a third party application. 

## Prototypes

### Web crawler

The client wanted a tool to crawl the site and look for potential broken links. While developing a prototype for this tool, we figured that we could double this tool up and also use it to help generate the databases needed for our text search functionality. A functioning version of the program can be viewed [here](https://github.com/zedchance/crawler).

### Persistent audio player

Our team put together multiple prototypes of a persistent audio player. This feature can be accomplished using HTML audio elements and the History API. While our prototype was more of a proof of concept, it showed the team exactly what type of technologies we will need to use to implement the feature.

### Speech to text transcription

We will be using the open source [Mozilla DeepSpeech](https://github.com/mozilla/DeepSpeech) speech-to-text engine to provide audio transcription for the recordings.

## Timeline

1. Migrate site to new server
2. Migrate database to PostgreSQL
3. Implement persistent footer
4. Implement advanced search
5. Transcribe audio recordings
