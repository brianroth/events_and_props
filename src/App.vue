<template>
   <div id="app" >
      <app-artist :artist="artist"></app-artist>
      <div class="container">
        <template v-for="album in albums">
          <app-album :album="album"></app-album>
        </template>
      </div>
   </div>
</template>

<script>
import Album from './Album.vue'
import Artist from './Artist.vue'

export default {
  data () {
    return {
      artist: {
        name: 'Led Zepplin',
        url: 'https://en.wikipedia.org/wiki/Led_Zeppelin',
        blurb: `Led Zeppelin were an English rock band formed in London in 1968. The group consisted of guitarist Jimmy Page, singer Robert Plant, bassist and keyboardist John Paul Jones, and drummer John Bonham. The band's heavy, guitar-driven sound has led them to be cited as one of the progenitors of heavy metal, though their unique style drew from a wide variety of influences, including blues, psychedelia, and folk music.`,
        likes: 0
      },
      albums: [
        {
          title: 'Led Zeppelin',
          year: 1969,
          liked: false,
          url: 'https://en.wikipedia.org/wiki/Led_Zeppelin_(album)',
          image: 'https://upload.wikimedia.org/wikipedia/en/e/ef/Led_Zeppelin_-_Led_Zeppelin_%281969%29_front_cover.png',
          blurb: `Led Zeppelin is the eponymous debut studio album by English rock band Led Zeppelin, released on 12 January 1969 in the United States and on 31 March 1969 in the United Kingdom by Atlantic Records. Featuring integral contributions from each of the group's four members, the album was recorded in October 1968 at Olympic Studios in London and established their fusion style of both blues and rock music. It also attracted a large and devoted following to the band; Zeppelin's take on the emerging hard rock sound endeared them to parts of the counterculture on both sides of the Atlantic Ocean.`,
          tracks: [
            { number: 1, liked: false,title: 'Good Times Bad Times', length: 166 },
            { number: 2, liked: false,title: "Babe I'm Gonna Leave You", length: 402 },
            { number: 3, liked: false,title: "You Shook Me", length: 388 },
            { number: 4, liked: false,title: "Dazed and Confused"  , length: 388 },
            { number: 5, liked: false,title: "Your Time Is Gonna Come" , length: 274 },
            { number: 6, liked: false,title: "Black Mountain Side", length: 132 },
            { number: 7, liked: false,title: "Communication Breakdown", length: 150 },
            { number: 8, liked: false,title: "I Can't Quit You Baby", length: 322 },
            { number: 9, liked: false,title: "How Many More Times", length: 507 },
          ]
        },
        {
          title: 'Led Zeppelin II',
          year: 1969,
          url: 'https://en.wikipedia.org/wiki/Led_Zeppelin_II',
          image: 'https://upload.wikimedia.org/wikipedia/en/2/20/Led_Zeppelin_-_Led_Zeppelin_II.jpg',
          blurb: `Led Zeppelin II is the eponymous second studio album by the English rock band Led Zeppelin, released on 22 October 1969 in the United States and on 31 October 1969 in the United Kingdom by Atlantic Records. Recording sessions for the album took place at several locations in both the United Kingdom and North America from January to August 1969. The album's production was credited to the band's lead guitarist and songwriter Jimmy Page, and it also served as Led Zeppelin's first album to utilise the recording techniques of the engineer Eddie Kramer. Incorporating several elements of blues and folk music, Led Zeppelin II exhibited the band's evolving musical style of blues-derived material and their guitar riff-based sound. It has been described as the band's heaviest album.`,
          tracks: [
            { number: 1, liked: false, title: "Whole Lotta Love", length: 334 },
            { number: 2, liked: false, title: "What Is and What Should Never Be", length: 286 },
            { number: 3, liked: false, title: "The Lemon Song", length: 379 },
            { number: 4, liked: false, title: "Thank You", length: 329 },
            { number: 5, liked: false, title: "Heartbreaker", length: 294 },
            { number: 6, liked: false, title: "Living Loving Maid (She's Just a Woman)", length: 159 },
            { number: 7, liked: false, title: "Ramble On", length: 314 },
            { number: 8, liked: false, title: "Moby Dick", length: 300 },
            { number: 9, liked: false, title: "Bring It On Home", length: 299 }
          ]
        },
        { 
          title: 'Led Zeppelin III',
          year: 1970,
          url: 'https://en.wikipedia.org/wiki/Led_Zeppelin_III',
          image: 'https://upload.wikimedia.org/wikipedia/en/5/5f/Led_Zeppelin_-_Led_Zeppelin_III.png',
          blurb: `Led Zeppelin III is the eponymous third studio album by the English rock band Led Zeppelin, released on 5 October 1970 by Atlantic Records in the United States and on 23 October 1970 in the United Kingdom. The songs were written largely at a remote cottage in Wales known as Bron-Yr-Aur and recorded between May and August 1970. The album represented a maturing of the band's music towards a greater emphasis on folk and acoustic sounds. This surprised many fans and critics, and upon its release the album received rather indifferent reviews.
Led Zeppelin III is generally praised and acknowledged as representing an important milestone in the band's history, and a turning point in their music. Although acoustic songs had been featured on its predecessors, this album showed that Led Zeppelin were more than just a conventional rock band, and that they could branch out into wider musical territory, like folk.`,
          tracks: [
            { number: 1, liked: false, title: "Immigrant Song", length: 146 },
            { number: 2, liked: false, title: "Friends", length: 235 },
            { number: 3, liked: false, title: "Celebration Day", length: 209 },
            { number: 4, liked: false, title: "Since I've Been Loving You", length: 445 },
            { number: 5, liked: false, title: "Out on the Tiles" , length: 244 },
            { number: 6, liked: false, title: "Gallows Pole", length: 358 },
            { number: 7, liked: false, title: "Tangerine", length: 192 },
            { number: 8, liked: false, title: "That's the Way", length: 338 },
            { number: 9, liked: false, title: "Bron-Y-Aur Stomp" , length: 260 },
            { number: 10, liked: false, title: "Hats Off to (Roy) Harper", length: 221 }
          ]
        },
        { 
          title: 'Led Zeppelin IV', 
          year: 1971,
          url: 'https://en.wikipedia.org/wiki/Led_Zeppelin_IV',
          image: 'https://upload.wikimedia.org/wikipedia/en/2/26/Led_Zeppelin_-_Led_Zeppelin_IV.jpg',
          blurb: `The untitled fourth studio album by English rock band Led Zeppelin, commonly known as Led Zeppelin IV, was released on 8 November 1971 by Atlantic Records. Produced by guitarist Jimmy Page, it was recorded between November 1970 and January 1971 at several locations, most prominently the Victorian house Headley Grange.
After the band's previous album Led Zeppelin III received lukewarm reviews from critics, Page decided their fourth album would officially be untitled. This, along with the inner sleeve's design featuring four symbols that represented each band member, led to the album being referred to variously as the Four Symbols logo, Four Symbols, The Fourth Album, Untitled, Runes, The Hermit, and ZoSo (which was derived from Page's symbol). In addition to lacking an album title, the cover featured no band name, as the group wished to be anonymous and to avoid easy pigeonholing by the press.
Led Zeppelin IV was a commercial and critical success, featuring many of the band's best-known songs, including "Black Dog", "Rock and Roll", "Going to California" and "Stairway to Heaven". The album is one of the best-selling albums of all time with more than 37 million copies sold. It is tied for third highest-certified album in the United States by the Recording Industry Association of America at 23× Platinum. Writers and critics have regularly cited it on lists of the greatest albums of all time.`,
          tracks: [
            { number: 1, liked: false, title: "Black Dog", length: 294 },
            { number: 2, liked: false, title: "Rock and Roll", length: 220 },
            { number: 3, liked: false, title: "The Battle of Evermore", length: 351 },
            { number: 4, liked: false, title: "Stairway to Heaven", length: 482 },
            { number: 5, liked: false, title: "Misty Mountain Hop", length: 278 },
            { number: 6, liked: false, title: "Four Sticks", length: 284 },
            { number: 7, liked: false, title: "Going to California", length: 211 },
            { number: 8, liked: false, title: "When the Levee Breaks", length: 427 }
          ]
        },
        { 
          title: 'Houses of the Holy',
          year: 1973,
          url: 'https://en.wikipedia.org/wiki/Houses_of_the_Holy',
          image: 'https://upload.wikimedia.org/wikipedia/en/9/9f/Led_Zeppelin_-_Houses_of_the_Holy.jpg',
          blurb: `Houses of the Holy is the fifth studio album by the English rock band Led Zeppelin, released on 28 March 1973 by Atlantic Records. It is their first album composed of entirely original material and it represents a turning point in musical direction for the band, who had begun to record songs with more layering and production techniques.
Containing some of the band's most famous songs, including "The Song Remains the Same", "The Rain Song", and "No Quarter", Houses of the Holy became a commercial success, and was later certified 11x platinum by the Recording Industry Association of America (RIAA) in 1999. In 2012, the album was ranked at #148 on Rolling Stone's 500 Greatest Albums of All Time. The title track was originally recorded for the album, but was delayed until the release of band's next album Physical Graffiti in 1975.`,
          tracks: [
            { number: 1, liked: false, title: "The Song Remains the Same", length: 332 },
            { number: 2, liked: false, title: "The Rain Song", length: 459 },
            { number: 3, liked: false, title: "Over the Hills and Far Away", length: 290 },
            { number: 4, liked: false, title: "The Crunge", length: 197 },
            { number: 5, liked: false, title: "Dancing Days", length: 223 },
            { number: 6, liked: false, title: "D'yer Mak'er", length: 303 },
            { number: 7, liked: false, title: "No Quarter", length: 420 },
            { number: 8, liked: false, title: "The Ocean", length: 271 }
          ]
        },
        { 
          title: 'Physical Graffiti',
          year: 1975,
          url: 'https://en.wikipedia.org/wiki/Physical_Graffiti',
          image: 'https://upload.wikimedia.org/wikipedia/en/e/e3/Led_Zeppelin_-_Physical_Graffiti.jpg',
          blurb: `Physical Graffiti is the sixth studio album by the English rock band Led Zeppelin, released as a double album on 24 February 1975 by their newly founded imprint label Swan Song Records. The band wrote and recorded eight new songs for the album at Headley Grange, which stretched the total time of the record beyond the typical length of a single LP, so the band decided to make Physical Graffiti a double album by including unreleased tracks from earlier recording sessions: one outtake from Led Zeppelin III, three from Led Zeppelin IV, and three from Houses of the Holy, including the unused title track from the latter album.
Physical Graffiti was commercially and critically successful upon its release and debuted at number one on album charts in both the US and the UK. The album was later certified 16x platinum in the United States by the Recording Industry Association of America (RIAA) in 2006, signifying shipments of over eight million copies.`,
          tracks: [
            { number: 1, liked: false, title: "Custard Pie", length: 255 },
            { number: 2, liked: false, title: "The Rover", length: 339 },
            { number: 3, liked: false, title: "In My Time of Dying", length: 668 },
            { number: 4, liked: false, title: "Houses of the Holy", length: 244 },
            { number: 5, liked: false, title: "Trampled Under Foot", length: 336 },
            { number: 6, liked: false, title: "Kashmir", length: 517 },
            { number: 7, liked: false, title: "In the Light", length: 527 },
            { number: 8, liked: false, title: "Bron-Yr-Aur", length: 126 },
            { number: 9, liked: false, title: "Down by the Seaside", length: 315 },
            { number: 10, liked: false, title: "Ten Years Gone", length: 394 },
            { number: 11, liked: false, title: "Night Flight", length: 218 },
            { number: 12, liked: false, title: "The Wanton Song", length: 248 },
            { number: 13, liked: false, title: "Boogie with Stu", length: 232 },
            { number: 14, liked: false, title: "Black Country Woman", length: 264 },
            { number: 15, liked: false, title: "Sick Again" , length: 282 }
          ]
        },
        { 
          title: 'Presence', 
          year: 1976,
          url: 'https://en.wikipedia.org/wiki/Presence_(album)',
          image: 'https://upload.wikimedia.org/wikipedia/en/f/f3/Led_Zeppelin_-_Presence.jpg',
          blurb: `Presence is the seventh studio album by the English rock band Led Zeppelin, released by Swan Song Records on 31 March 1976. The album was a commercial success, reaching the top of both the British and American album charts, and achieving a triple-platinum certification in the United States, despite receiving mixed reviews from critics and being the slowest-selling studio album by the band (other than the outtake album Coda).
It was written and recorded during a tumultuous time in the band's history, as singer Robert Plant was recuperating from serious injuries he had sustained the previous year in a car accident. Nevertheless, guitarist Jimmy Page describes Presence as the band's "most important" album, proving they would continue and succeed despite their turmoil.`,
          tracks: [
            { number: 1, liked: false, title: "Achilles Last Stand", length: 630 },
            { number: 2, liked: false, title: "For Your Life", length: 381 },
            { number: 3, liked: false, title: "Royal Orleans", length: 179 },
            { number: 4, liked: false, title: "Nobody's Fault but Mine", length: 376 },
            { number: 5, liked: false, title: "Candy Store Rock", length: 268 },
            { number: 6, liked: false, title: "Hots On for Nowhere", length: 284 },
            { number: 7, liked: false, title: "Tea for One", length: 563 },
          ]
        },
        { 
          title: 'The Song Remains the Same',
          year: 1976,
          url: 'https://en.wikipedia.org/wiki/The_Song_Remains_the_Same_(album)',
          image: 'https://upload.wikimedia.org/wikipedia/en/b/b4/Led_Zeppelin_-_The_Song_Remains_the_Same.jpg',
          blurb: `The Song Remains the Same is the live soundtrack album of the concert film of the same name by the English rock band Led Zeppelin. The album was originally released in October 1976, before being remastered and reissued in 2007.`,
          tracks: [
            { number: 1, liked: false, title: "Rock and Roll (Live)", length: 243 },
            { number: 2, liked: false, title: "Celebration Day (Live)", length: 229 },
            { number: 3, liked: false, title: "The Song Remains the Same (Live)", length: 360 },
            { number: 4, liked: false, title: "The Rain Song (Live)", length: 505 },
            { number: 5, liked: false, title: "Dazed and Confused (Live)", length: 1613 },
            { number: 6, liked: false, title: "No Quarter (Live)", length: 750 },
            { number: 7, liked: false, title: "Stairway to Heaven (Live)", length: 658 },
            { number: 8, liked: false, title: "Moby Dick (Live)", length: 767 },
            { number: 9, liked: false, title: "Whole Lotta Love (Live)", length: 865 }
          ]
        },
        { 
          title: 'In Through the Out Door', 
          year: 1979,
          url: 'https://en.wikipedia.org/wiki/In_Through_the_Out_Door',
          image: 'https://upload.wikimedia.org/wikipedia/en/b/ba/Led_Zeppelin_-_In_Through_the_Out_Door.jpg',
          blurb: `In Through the Out Door is the eighth studio album by the English rock band Led Zeppelin, and their final album of entirely new material. It was recorded over a three-week period in November and December 1978 at ABBA's Polar Studios in Stockholm, Sweden, and released by Swan Song Records on 15 August 1979. In Through the Out Door was the band's eighth and final studio release to reach the top of the charts in America, and was the last released by the band before the death of drummer John Bonham in 1980.
The album is a reflection of the personal turmoil that the band members had been going through before and during its recording. For example, frontman Robert Plant and his wife had gone through a serious car accident, and their young son, Karac Plant, died from a stomach illness. All four band members also felt weary of dealing with record companies and other associates. Despite this, the release wound up being a huge commercial success, particularly in the United States (sitting at the #1 slot on Billboard's chart in just its second week on the chart).`,
          tracks: [
            { number: 1, liked: false, title: "In the Evening", length: 413 },
            { number: 2, liked: false, title: "South Bound Saurez", length: 253 },
            { number: 3, liked: false, title: "Fool in the Rain", length: 370 },
            { number: 4, liked: false, title: "Hot Dog", length: 198 },
            { number: 5, liked: false, title: "Carouselambra", length: 634 },
            { number: 6, liked: false, title: "All My Love", length: 353 },
            { number: 7, liked: false, title: "I'm Gonna Crawl", length: 329 }
          ]
        },
        { 
          title: 'Coda', 
          year: 1982,
          url: 'https://en.wikipedia.org/wiki/Coda_(album)',
          image: 'https://upload.wikimedia.org/wikipedia/commons/c/c1/Led_Zeppelin_-_Coda.jpg',
          blurb: `Coda is the ninth and final studio album[12] by the English rock band Led Zeppelin, released in 1982. The album is a collection of unused tracks from various sessions during Led Zeppelin's twelve-year career. It was released two years after the group had officially disbanded following the death of drummer John Bonham. The word coda, meaning a passage that ends a musical piece following the main body, was therefore chosen as the title.`,
          tracks: [
            { number: 1, liked: false, title: "We're Gonna Groove", length: 157 },
            { number: 2, liked: false, title: "Poor Tom", length:  182 },
            { number: 3, liked: false, title: "I Can't Quit You Baby", length: 298 },
            { number: 4, liked: false, title: "Walter's Walk", length: 511 },
            { number: 5, liked: false, title: "Ozone Baby", length: 216 },
            { number: 6, liked: false, title: "Darlene", length: 306 },
            { number: 7, liked: false, title: "Bonzo's Montreux", length: 262 },
            { number: 8, liked: false, title: "Wearing and Tearing", length: 327 }
          ]
        }
      ]
    }
  },
  components: {
    appAlbum: Album,
    appArtist: Artist
  }
}
</script>
