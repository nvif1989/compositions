Detailed [nutrient composition] of 592 key foods in India.
> This is part of package [nvif1989].<br>
> Source: [Nutritive Value of Indian Foods 1989].

```javascript
const compositions = require('@nvif1989/compositions');
// compositions.corpus: Map {code => {code, name, scie, lang, grup, tags, ...}}
// compositions.load(): Promise (corpus loaded)
// compositions.sql([table], [options]): Promise (sql commands)
// compositions.csv(): path to csv file
// compositions(<query>)
// -> [{code, name, scie, lang, grup, tags, ...}] for matched foods


async function main() {
await compositions.load();
/* load corpus first */

// NOTE: grup is wrong, curd is wrong
compositions('pine apple');
compositions('ananas comosus');
compositions('sapuri');
compositions('294');
// [
//   {
//     code: '294',
//     name: 'PINE APPLE',
//     scie: 'Ananas comosus',    lang: 'B. Anarash; G., H., Kan., Mar., P. Ananas; Mal. Kayitha chakka; O. Sapuri Anasianas; Tam. Anasi pazham; Tel. Anasa Pandu',
//     grup: 'Cereal grains and products',
//     tags: 'vegetarian eggetarian fishetarian veg',
//     enerc: 46,
//     water: 87.8,
//     ...
//   }
// ]

compositions('tell me about khoa.');
// [
//   {
//     code: '430',
//     name: 'KHOA (skimmed buffalo milk)',
//     scie: '',
//     lang: 'B., H., Kan., Mal., P., Tel. Khoa; O. Kua; Tam. Thirattu pal',
//     grup: 'Milk and Milk products',
//     tags: 'vegetarian eggetarian fishetarian veg',
//     enerc: 206,
//     water: 46.1,
//     ...
//   },
//   {
//     code: '429',
//     name: 'KHOA (whole buffalo milk)',
//     scie: '',
//     lang: '',
//     grup: 'Milk and Milk products',
//     tags: 'vegetarian eggetarian fishetarian veg',
//     enerc: 421,
//     water: 30.6,
//     ...
//   },
//   {
//     code: '431',
//     name: "KHOA (whole cow's milk)",
//     scie: '',
//     lang: 'B. Makhantana doodh; Kash Gurus; Mal. Padakalanya pal, O. Sarakadha dudha; Tam. Kudaintha pal; Tel. Venna theesina palu',
//     grup: 'Milk and Milk products',
//     tags: 'vegetarian eggetarian fishetarian veg',
//     enerc: 413,
//     water: 25.2,
//     ...
//   }
// ]
}
main();
```


[![nvif1989](https://i.imgur.com/mGVou5c.png)](https://www.npmjs.com/package/nvif1989)
> You can ask about composition of 592 key foods in India here: [nvif1989.github.io].<br>
> Food composition values were measured by [National Institute of Nutrition, Hyderabad].<br>
> Take a peek at the raw data here: [CSV].

[nvif1989]: https://www.npmjs.com/package/nvif1989
[Nutritive Value of Indian Foods 1989]: https://www.icmr.nic.in/content/nutritive-value-indian-foods-nvif-c-gopalan-b-v-rama-sastri-sc-balasubramanian-revised
[nutrient composition]: https://github.com/nvif1989/compositions/blob/master/index.csv
[CSV]: https://github.com/nvif1989/compositions/blob/master/assets/
[nvif1989.github.io]: https://nvif1989.github.io
[National Institute of Nutrition, Hyderabad]: https://www.nin.res.in/
[Document]: https://docs.google.com/spreadsheets/d/1mQgRIU0EO8t1ZT72Fc6qAgcWBoqBTMK-gYl5fS9CrFE/edit?usp=sharing
[Webpage]: https://docs.google.com/spreadsheets/d/e/2PACX-1vSrD1oY4lNHWpBxzKsnYW9RelZDksfhuDITKyqGqUYAu69V6EyeIe7RajqxxKNu6_bCAg5Il7mB1WGC/pubhtml
