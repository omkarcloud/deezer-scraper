# Deezer Scraper

Deezer Scraper gets you 🎯 accurate, 🔍 detailed Deezer data as clean JSON in **Real-Time**.

No selectors, no proxies, no data cleaning. Just the data.

[**Try it now in the playground**](https://www.omkar.cloud/tools/deezer-scraper/playground) - See the data quality for yourself in one click, **No sign-up required**.

**Build on it free:** 1,000 calls every month, no credit card ❤️

[![Deezer Scraper API playground — run a live request in your browser, free, no sign-up](https://raw.githubusercontent.com/omkarcloud/deezer-scraper/master/playground.png)](https://www.omkar.cloud/tools/deezer-scraper/playground)

## What can I get

- 🎵 **Full track records** — ISRC, BPM, replay gain, release dates, per-role credits, streaming rights and availability in 209 countries, plus a 30-second preview MP3
- 🔎 **Search everything** — artists, tracks, albums, playlists, users, podcasts and live radios in one call, with autocomplete and advanced artist / album / label filters
- 🎤 **Artists, albums & playlists** — bios, fan counts, top tracks, full discographies, related artists, tracklists with UPCs and ISRCs, playlists with the date each track was added
- 📈 **Charts & genres for any country** — today's top tracks, albums, artists, playlists and podcasts per market and genre, 120M+ tracks behind it

## Why Deezer Scraper

Most other Deezer APIs fail you in one of four ways:

- 🗄️ **Inaccurate, cached, stale data**
- 🧩 **Low-detail endpoints** — a few fields per call, never the full picture
- 💸 **Pay more to get the same data**
- 🪦 **Works today, breaks next month** — nobody maintains it

Deezer Scraper is scraped live on every call, priced honestly, and actively maintained.

Deezer geo-gates its catalogue by IP — charts, search ranking and availability differ per country. Deezer Scraper routes every call through the market you ask for (`country`, default `us`), so you get exactly what a listener there sees.

## Example: A Full Deezer Track

```json
{
  "id": 3135556,
  "title": "Harder, Better, Faster, Stronger",
  "link": "https://www.deezer.com/track/3135556",
  "preview_link": "https://cdnt-preview.dzcdn.net/api/1/1/6/a/2/0/6a2c0a5670afe821e08fc5154909534a.mp3?...",
  "isrc": "GBDUW0000059",
  "duration_seconds": 226,
  "release_date": "2001-03-12",
  "track_position": 4,
  "disk_number": 1,
  "bpm": null,
  "gain_db": -12.4,
  "rank": 810329,
  "copyright": "\u00a9 2001 Daft Life Limited",
  "is_explicit_lyrics": false,
  "explicit_lyrics_status": "not_explicit",
  "credits": { "main_artists": ["Daft Punk"], "authors": ["Edwin Birdsong", "Guy-Manuel de Homem-Christo", "Thomas Bangalter"] },
  "artist": { "id": 27, "name": "Daft Punk", "link": "https://www.deezer.com/artist/27", "pictures": { "xl": "https://cdn-images.dzcdn.net/images/artist/638e69b9caaf9f9f3f8826febea7b543/1000x1000-000000-80-0-0.jpg" } },
  "album": { "id": 302127, "title": "Discovery", "link": "https://www.deezer.com/album/302127", "release_date": "2001-03-07", "cover": { "xl": "https://cdn-images.dzcdn.net/images/cover/5718f7c81c27e0b2417e2a4c45224f8a/1000x1000-000000-80-0-0.jpg" } },
  "availability": { "country": "us", "is_available_in_country": true, "country_count": 209, "countries": ["AE", "AF", "AG", "..."], "is_free_stream_available": true, "is_subscription_stream_available": true },
  "related_albums": [
    { "id": 302127, "title": "Discovery", "release_date": "2001-03-12", "is_streamable": true },
    { "id": 302378, "title": "Harder, Better, Faster, Stronger", "release_date": "2001-10-19", "is_streamable": true }
  ],
  "updated_at": "2026-03-04T01:47:10Z"
}
```

*Trimmed for readability.*

## Get Started with 1,000 Free Calls

Start in the [playground](https://www.omkar.cloud/tools/deezer-scraper/playground) — try any endpoint with one click, no sign-up required.

Once you're happy with the data, start with the free plan for 1,000 free calls every month:

1. [Sign up on Omkar Cloud](https://www.omkar.cloud/auth/sign-up?redirect=/tools/deezer-scraper/playground) — free, no credit card.
2. Open the [Deezer Scraper playground](https://www.omkar.cloud/tools/deezer-scraper/playground) and enter any artist, track, album or playlist you like. Click **Get Live Data**.
3. Enjoy your data 😎.

## Endpoints

26 endpoints cover everything you need.

| Endpoint | Path | Returns |
|---|---|---|
| Track Details | `/tracks/details` | Everything about one recording: ISRC, BPM, credits, rights, availability, artist, album and other releases |
| Search All | `/search/all` | Top result plus artists, tracks, albums, playlists, users, podcasts and live radios for a query |
| Search Autocomplete | `/search/auto-complete` | Search-box completions, exactly as Deezer suggests them |
| Search Tracks / Albums / Artists / Playlists / Users / Podcasts | `/search/tracks`, `/search/albums`, `/search/artists`, `/search/playlists`, `/search/users`, `/search/podcasts` | One page per kind, 25 per page up to 100, with advanced filters on tracks and strict matching |
| Album Details / Tracks | `/albums/details`, `/albums/tracks` | UPC, covers, dates, label, genres, credits, full tracklist with ISRCs and previews |
| Artist Details / Top Tracks / Albums / Related / Playlists / Radio | `/artists/details`, `/artists/top-tracks`, `/artists/albums`, `/artists/related`, `/artists/playlists`, `/artists/radio` | Bio, fans, links, latest release, discography, similar artists, playlists and Deezer's artist mix |
| Playlist Details / Tracks | `/playlists/details`, `/playlists/tracks` | Header, creator, counts and every track with the date it was added |
| Charts / Tracks / Albums / Artists / Playlists / Podcasts | `/charts/list`, `/charts/tracks`, `/charts/albums`, `/charts/artists`, `/charts/playlists`, `/charts/podcasts` | Today's charts for any country, optionally within a genre, with positions |
| Genres | `/genres/list` | Deezer's genre catalogue with the ids the chart endpoints accept |

## Pricing

High value, Low price.

| Plan | Price | Calls / month | Per 1,000 |
|---|---|---|---|
| **Basic** | **Free** | **1,000** — the most generous free plan | $0 |
| **Pro** | $16/mo | 20,000 | $0.80 |
| **Ultra** | $48/mo | 100,000 | $0.48 |
| **Mega** | $148/mo | 400,000 | $0.37 |

Need a bigger plan? Ask on [WhatsApp](https://api.whatsapp.com/send?phone=918178804274&text=I%20need%20a%20custom%20plan%20for%20the%20Deezer%20Scraper%20API.) or [Email](mailto:happy.to.help@omkar.cloud?subject=Custom%20plan%20for%20Deezer%20Scraper%20API&body=I%20need%20a%20custom%20plan%20for%20the%20Deezer%20Scraper%20API.).

- [**90 Day 2 Click Refund Guarantee**](https://www.omkar.cloud/refund-process)
- This is an excellent API made by Omkar Cloud, which is Rated Excellent — [4.7 based on 30 reviews on Trustpilot](https://www.trustpilot.com/review/omkar.cloud).

👉 [Start with Free Plan](https://www.omkar.cloud/auth/sign-up?redirect=/tools/deezer-scraper/playground) — 1,000 free calls/month

## 💬 Have Questions? We Have Answers.

You're a developer — we know how hard completing a project can be. So we offer full support: just message us and we'll reply ✅ with a solution within 1 working day.

[![Message Us on WhatsApp about Deezer Scraper](https://raw.githubusercontent.com/omkarcloud/assets/master/images/whatsapp-us.png)](https://api.whatsapp.com/send?phone=918178804274&text=I%20need%20help%20using%20the%20Deezer%20Scraper%20API.)

[![Ask Us by Email about Deezer Scraper](https://raw.githubusercontent.com/omkarcloud/assets/master/images/ask-on-email.png)](mailto:happy.to.help@omkar.cloud?subject=Help%20with%20Deezer%20Scraper%20API&body=I%20need%20help%20using%20the%20Deezer%20Scraper%20API.)

## Popular Scrapers by Omkar Cloud

- [**Google Maps Scraper (3,100+ GitHub Stars)**](https://github.com/omkarcloud/google-maps-scraper) — type "record labels in Los Angeles", get every business as a ready-to-call lead list: phones, emails, websites & reviews. Up to 100K free leads/month.
- [**IMDb Scraper**](https://www.omkar.cloud/tools/imdb-scraper) — movies, TV, ratings, cast, charts & box office
- [**Skyscanner Scraper**](https://www.omkar.cloud/tools/skyscanner-scraper) — live flights, every agent's price, cheapest months & hotels
- [**Booking Scraper**](https://www.omkar.cloud/tools/booking-scraper) — Booking.com hotels: prices, ratings, rooms & amenities
- [**Website Email Contact Scraper**](https://www.omkar.cloud/tools/website-email-contact-scraper) — emails, phones & socials from any website
- [**AliExpress Scraper**](https://www.omkar.cloud/tools/aliexpress-scraper) — live product details, SKU variants, stock & shipping

👉 [Start with Free Plan](https://www.omkar.cloud/auth/sign-up?redirect=/tools/deezer-scraper/playground) — 1,000 free calls/month
