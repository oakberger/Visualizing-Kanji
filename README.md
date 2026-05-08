# Visualizing-Kanji

A repo that visualizes the connection between the Kanji I learned in my Japanese A1.2 course using Obsidian graph view.

![Graph Visualization](Attachments/visualization.gif)

The course follows the Genki I book. We had to learn the Kanji along with the orange highlighted words from chapter 3 - 8 (page 304 - 330). There are 86 unique Kanji and I noticed that the actual words often shared a lot of the same Kanji. So I thought it could be interesting to try to visualize this using Obsidian's graph view.

My approach was to create a `.md` file for each Japanese word, and to link it to the Kanji that the word was made of. Additionally, to be able to practice the kanji, I also linked all the words and Kanji to their corresponding english and hiragana translation.

> **Example:** "先生" (teacher) is linked to "先" (ahead) and "生" (birth) as well as to "teacher" and "せんせい"

---

## Explanation of the Tags

| Tag                      | Description                                                                                                                                                                                                                                                    |
| ------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `Japanese-Word`          | All the actual words we had to learn. _e.g. 先生 (teacher), 会う (to meet), 車 (car)_                                                                                                                                                                               |
| `Kanji-Symbol`           | The individual building blocks which build up most Japanese words. _e.g. 先 (ahead), 生 (birth)_. Mostly used in combination with other Kanji, but occasionally used individually _e.g. 車 (car)_. These are tagged with both `Japanese-Word` and `Kanji-Symbol`. |
| `English-Translation`    | The English translation of all the Japanese words.                                                                                                                                                                                                             |
| `English-Meaning`        | The approximate translation / meaning of the Kanji symbols that are usually not used by themselves. Again there are words tagged with both `English-Translation` and `English-Meaning`.                                                                        |
| `Japanese-Pronunciation` | The hiragana translation of the Japanese words. Used for understanding how to pronounce the words.                                                                                                                                                             |
| `Kanji-Pronunciation`    | The hiragana translation of the Kanji symbols. Used for understanding how to pronounce the Kanji.                                                                                                                                                              |
| `English`                | All English words additionally receive this tag. Makes it easier to toggle them on and off in the graph view.                                                                                                                                                  |
| `Hiragana`               | All hiragana words additionally receive this tag. Also makes it easier to toggle them in the graph view.                                                                                                                                                       |

---

## Explanation of the Graph View

The graph view shows all the linked files. By adjusting the Display and Forces settings I found an optimal viewpoint that ideally visualizes the connections between the Kanji.

The filters `-path:Main -path:Templates -file:README` are applied so that only the wanted words are displayed. The three most important groups `tag:#Kanji-Symbol`, `tag:#Japanese-Word` and `tag:#English` are added in the Groups dropdown and given distinct colors. Additionally the filters `-tag:English` and `-tag:Hiragana` can be applied if only the connection of the Kanji should be visualized.

The community plugin **Extended Graph** is used to increase the size of the text of the nodes when hovering over them and to import the default state of the graph view. The text size is increased with the CSS snippet in `~/.obsidian/snippets`:

```css
.graph-view.node-text { font-size: 20px; }
```