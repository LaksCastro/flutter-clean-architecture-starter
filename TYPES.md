<details>
  <summary>Work</summary>
  <br>
  <ul>
    <li>
      <div>
        <p>Interface</p>

```ts
interface Work {
  id: number;
  user: User;
  image_url: string;
  ogp_image_url: string;
  share_url: string;
  title: string;
  text: string;
  color_codes: ColorCode[];
  like_count: number;
  tags: string[];
  width: number;
  height: number;
  created_at: number;
  is_like: boolean;
  allow_thread: boolean;
}
```

<br>
      </div>
    </li>
    <li>
      <div>
        <p>Example</p>
        
```ts
const work : Work {
  id: 2076467,
  user: User,
  image_url: "https://img.dotpicko.net/72b4d2892de744ee5528c90a8bcfe13654307b98267e7b4e099ed80bc4f83551.png",
  ogp_image_url: "https://img.dotpicko.net/ogp_72b4d2892de744ee5528c90a8bcfe13654307b98267e7b4e099ed80bc4f83551.png",
  share_url: "https://dotpict.net/works/2076467",
  title: "Canvas6",
  text: "",
  color_codes: ColorCode[],
  like_count: 0,
  tags: ["people"],
  width: 128,
  height: 128,
  created_at: 1597896817,
  is_like: false,
  allow_thread: true,
}
```
<br>
      </div>
    </li>
  </ul>
</details>

<details>
  <summary>RankedWork</summary>
  <br>
  <ul>
    <li>
      <div>
        <p>Interface</p>

```ts
interface RankedWork {
  rank: number;
  work: Work;
}
```

<br>
      </div>
    </li>
    <li>
      <div>
        <p>Example</p>
        
```ts
const rankedWork : RankedWork {
  rank: 1,
  work: Work,
}
```
<br>
      </div>
    </li>
  </ul>
</details>

<details>
  <summary>User</summary>
  <br>
  <ul>
    <li>
      <div>
        <p>Interface</p>

```ts
interface User {
  id: number;
  name: string;
  account: string;
  text: string;
  url: string;
  share_url: string;
  profile_image_url: string;
  is_followed: boolean;
  is_banned: boolean;
  followed_count: number;
  follower_count: number;
  is_verified: boolean;
}
```

<br>
      </div>
    </li>
    <li>
      <div>
        <p>Example</p>

```ts
const user: User = {
  id: 453197,
  name: "にわしか",
  account: "",
  text: "おおきくなったらゔれいんずとけっこんするんだ",
  url: "https://www.pixiv.net/users/31989750",
  share_url: "https://dotpict.net/users/453197",
  profile_image_url:
    "https://img.dotpicko.net/523512246c9e0354cefa1acdecd14157d261af1d73231eb532b398040e815cbd.png",
  is_followed: false,
  is_banned: false,
  followed_count: 0,
  follower_count: 0,
  is_verified: true,
};
```

<br>
      </div>
    </li>
  </ul>
</details>

<details>
  <summary>ColorCode</summary>
  <br>
  <ul>
    <li>
      <div>
        <p>Interface</p>

```ts
interface ColorCode {
  red: number;
  green: number;
  blue: number;
  alpha: number;
}
```

<br>
      </div>
    </li>
    <li>
      <div>
        <p>Example</p>
        
```ts
const colorCode : ColorCode {
  red: 209,
  green: 133,
  blue: 196,
  alpha: 255,
}
```
<br>
      </div>
    </li>
  </ul>
</details>
