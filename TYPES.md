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
const work : Work = {
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
  <summary>Work</summary>
  <br>
  <ul>
    <li>
      <div>
        <p>Interface</p>

```ts
interface WorkThread {
  id: number;
  parent_id: number;
  work_id: number;
  user: User;
  text: string;
  comment_count: number;
  thread_count: number;
  is_liked_by_author: boolean;
  created_at: number;
}
```

<br>
      </div>
    </li>
    <li>
      <div>
        <p>Example</p>
        
```ts
const workThread : WorkThread = {
  id: 492920,
  parent_id: 0,
  work_id: 1111111,
  user: User,
  text: "まさかの34。",
  comment_count: 0,
  thread_count: 0,
  is_liked_by_author: false,
  created_at: 1562329415
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
const rankedWork : RankedWork = {
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
  <summary>CarouselItem</summary>
  <br>
  <ul>
    <li>
      <div>
        <p>Interface</p>

```ts
interface CarouselItem {
  id: number;
  image_url: string;
  url: string;
  label: string;
  label_hex_color: string;
  title: string;
  text: string;
  by_name: string;
  author_id: number;
}
```

<br>
      </div>
    </li>
    <li>
      <div>
        <p>Example</p>
        
```ts
const carouselItem: CarouselItem = {
  id: 4,
  image_url: "https://storage.googleapis.com/making/ichiharune/ichiharune.png",
  url: "https://dotpict.net/making/ichiharune?noHeader=true&fromApp=true",
  label: "MAKING",
  label_hex_color: "#00C2FF",
  title: "The Girl on the Way Home from Shopping",
  text: "",
  by_name: "by Ichiharune",
  author_id: 2124,
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
const colorCode : ColorCode = {
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

<details>
  <summary>UserRelationship</summary>
  <br>
  <ul>
    <li>
      <div>
        <p>Interface</p>

```ts
interface UserRelationship {
  requested_user_id: number;
  target_user_id: number;
  is_blocked: boolean;
  is_muted: boolean;
}
```

<br>
      </div>
    </li>
    <li>
      <div>
        <p>Example</p>
        
```ts
const userRelationship: UserRelationship = {
  requested_user_id: 0,
  target_user_id: 453197,
  is_blocked: false,
  is_muted: false,
};
```
<br>
      </div>
    </li>
  </ul>
</details>

<details>
  <summary>UserSummary</summary>
  <br>
  <ul>
    <li>
      <div>
        <p>Interface</p>

```ts
interface UserSummary {
  user: User;
  works: Work[];
}
```

<br>
      </div>
    </li>
    <li>
      <div>
        <p>Example</p>
        
```ts
const userSummary: UserSummary = {
  user: User,
  works: Work[],
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
const colorCode : ColorCode = {
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
