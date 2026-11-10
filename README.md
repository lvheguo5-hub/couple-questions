# Couple Questions

682 original questions and prompts for couples, in 30 sets, as plain JSON.

They are the question sets behind [Free Couple Games](https://freecouplegames.com), a site of free browser games for two. Each set here can also be played online with no login: one question at a time, on one shared screen.

## What is in here

| Set | Category | Prompts | Play online |
| --- | --- | --- | --- |
| [Would You Rather](data/would-you-rather-for-couples.json) | Conversation | 12 | [Play](https://freecouplegames.com/games/would-you-rather-for-couples) |
| [21 Questions](data/21-questions-for-couples.json) | Conversation | 21 | [Play](https://freecouplegames.com/games/21-questions-for-couples) |
| [Couple Quiz](data/couple-quiz.json) | Conversation | 12 | [Play](https://freecouplegames.com/games/couple-quiz) |
| [This or That](data/this-or-that-questions-for-couples.json) | Conversation | 24 | [Play](https://freecouplegames.com/games/this-or-that-questions-for-couples) |
| [Finish My Sentence Game](data/finish-my-sentence-game.json) | Conversation | 10 | [Play](https://freecouplegames.com/games/finish-my-sentence-game) |
| [Two Truths One Lie](data/two-truths-one-lie-for-couples.json) | Deep Talk | 18 | [Play](https://freecouplegames.com/games/two-truths-one-lie-for-couples) |
| [Pillow Talk Questions](data/pillow-talk-questions.json) | Deep Talk | 24 | [Play](https://freecouplegames.com/games/pillow-talk-questions) |
| [Deep Questions](data/deep-questions-for-couples.json) | Deep Talk | 24 | [Play](https://freecouplegames.com/games/deep-questions-for-couples) |
| [36 Questions](data/36-questions-to-fall-in-love.json) | Deep Talk | 36 | [Play](https://freecouplegames.com/games/36-questions-to-fall-in-love) |
| [Hot Seat Questions](data/hot-seat-questions-for-couples.json) | Deep Talk | 24 | [Play](https://freecouplegames.com/games/hot-seat-questions-for-couples) |
| [Relationship Check In Questions](data/relationship-check-in-questions.json) | Deep Talk | 10 | [Play](https://freecouplegames.com/games/relationship-check-in-questions) |
| [Truth or Dare](data/truth-or-dare-for-couples.json) | Playful | 16 | [Play](https://freecouplegames.com/games/truth-or-dare-for-couples) |
| [Road Trip Games](data/road-trip-games-for-couples.json) | Playful | 24 | [Play](https://freecouplegames.com/games/road-trip-games-for-couples) |
| [Red or Green Flag](data/red-flag-green-flag-game.json) | Playful | 30 | [Play](https://freecouplegames.com/games/red-flag-green-flag-game) |
| [Would You Still Love Me If Questions](data/would-you-still-love-me-if-questions.json) | Playful | 15 | [Play](https://freecouplegames.com/games/would-you-still-love-me-if-questions) |
| [Couples Charades](data/charades-for-couples.json) | Party | 30 | [Play](https://freecouplegames.com/games/charades-for-couples) |
| [Emoji Decoder](data/emoji-decoder-for-couples.json) | Party | 24 | [Play](https://freecouplegames.com/games/emoji-decoder-for-couples) |
| [Couples Pictionary](data/pictionary-for-couples.json) | Party | 40 | [Play](https://freecouplegames.com/games/pictionary-for-couples) |
| [Rapid Fire Questions](data/rapid-fire-questions-for-couples.json) | Party | 30 | [Play](https://freecouplegames.com/games/rapid-fire-questions-for-couples) |
| [Word Guessing](data/word-guessing-for-couples.json) | Party | 30 | [Play](https://freecouplegames.com/games/word-guessing-for-couples) |
| [Most Likely To](data/most-likely-to-for-couples.json) | Party | 24 | [Play](https://freecouplegames.com/games/most-likely-to-for-couples) |
| [Never Have I Ever](data/never-have-i-ever-for-couples.json) | Party | 24 | [Play](https://freecouplegames.com/games/never-have-i-ever-for-couples) |
| [Newlywed Game](data/newlywed-game-questions.json) | Party | 30 | [Play](https://freecouplegames.com/games/newlywed-game-questions) |
| [Couples Drinking Game](data/drinking-games-for-couples.json) | Party | 30 | [Play](https://freecouplegames.com/games/drinking-games-for-couples) |
| [Fantasy Match](data/fantasy-match-for-couples.json) | Romantic | 18 | [Play](https://freecouplegames.com/games/fantasy-match-for-couples) |
| [Kiss Marry Kill](data/kiss-marry-kill-for-couples.json) | Romantic | 18 | [Play](https://freecouplegames.com/games/kiss-marry-kill-for-couples) |
| [Long Distance Date Ideas](data/long-distance-date-ideas.json) | Long Distance | 24 | [Play](https://freecouplegames.com/games/long-distance-date-ideas) |
| [Sync Watch Party](data/sync-watch-party.json) | Long Distance | 18 | [Play](https://freecouplegames.com/games/sync-watch-party) |
| [Long Distance Questions](data/long-distance-questions-for-couples.json) | Long Distance | 24 | [Play](https://freecouplegames.com/games/long-distance-questions-for-couples) |
| [Virtual Dinner Date](data/virtual-dinner-date-game.json) | Long Distance | 18 | [Play](https://freecouplegames.com/games/virtual-dinner-date-game) |

`data/index.json` lists every set with its category, prompt count and play link.

## Format

Each file in `data/` is one set:

```json
{
  "slug": "21-questions-for-couples",
  "title": "21 Questions",
  "category": "Conversation",
  "playOnline": "https://freecouplegames.com/games/21-questions-for-couples",
  "count": 21,
  "prompts": [
    { "prompt": "What ordinary moment with me would you happily repeat?" }
  ]
}
```

A prompt can also carry:

- `options`: the two choices, for Would You Rather and This or That.
- `mode`: `truth` or `dare`, for Truth or Dare.
- `section`: a group heading inside a set.

## Using it

Read a file and pick a prompt at random:

```js
import set from "./data/deep-questions-for-couples.json" with { type: "json" };

const pick = set.prompts[Math.floor(Math.random() * set.prompts.length)];
console.log(pick.prompt);
```

The prompts are written to work for new couples and long-term partners. They avoid scoring a relationship, and anything that pushes one person to answer. If you build with them, keep a way to skip.

## License

The questions are licensed under [CC BY 4.0](LICENSE). You can use and adapt them, including commercially, if you credit **Free Couple Games** with a link to https://freecouplegames.com.

## More

- [All couple games](https://freecouplegames.com/games)
- [Questions for couples, organized by situation](https://freecouplegames.com/questions-for-couples)
- [Games to play on a video call](https://freecouplegames.com/games-to-play-on-video-call)
- Found a typo or a prompt that reads badly? Open an issue.
