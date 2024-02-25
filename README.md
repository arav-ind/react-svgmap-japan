# React SVG Map Japan

This package generates an interactive SVG map of Japan. It allows users to highlight states on hover and retrieve the value of the selected state. The map includes all states and union territories of Japan.

![Japan Map](./svgmap.gif)

## Installation

Install the package via npm:

```bash
npm install react-svgmap-japan
```

## Prefecture List

The following are the prefectures mapped with ID.

```js
const prefectures = {
  AIC: 'Aichi',
  AKI: 'Akita',
  AOM: 'Aomori',
  CHB: 'Chiba',
  EHM: 'Ehime',
  FKU: 'Fukui',
  FKO: 'Fukuoka',
  FSH: 'Fukushima',
  GIF: 'Gifu',
  GNM: 'Gunma',
  HYG: 'Hyogo',
  HOK: 'Hokkaido',
  HRS: 'Hiroshima',
  IBR: 'Ibaraki',
  ISH: 'Ishikawa',
  IWT: 'Iwate',
  KCH: 'Kochi',
  KGG: 'Kagawa',
  KMT: 'Kumamoto',
  KNG: 'Kanagawa',
  KGS: 'Kagoshima',
  KYO: 'Kyoto',
  MIE: 'Mie',
  MGI: 'Miyagi',
  MYZ: 'Miyazaki',
  NGT: 'Niigata',
  NGN: 'Nagano',
  NRA: 'Nara',
  NGS: 'Nagasaki',
  OKN: 'Okinawa',
  OSK: 'Osaka',
  OKY: 'Okayama',
  OIT: 'Oita',
  SGA: 'Saga',
  SHG: 'Shiga',
  SHM: 'Shimane',
  STM: 'Saitama',
  SZK: 'Shizuoka',
  TCG: 'Tochigi',
  TKY: 'Tokyo',
  TSJ: 'Tokushima',
  TTR: 'Tottori',
  TYM: 'Toyama',
  WKM: 'Wakayama',
  YMG: 'Yamaguchi',
  YMN: 'Yamanashi',
  YGT: 'Yamagata'
}
```

## Japange

```jsx
'use client'

import { useState } from 'react'
import JapanMap from 'react-svgmap-Japan'

export default function MapComponent() {
    const [state, setState] = useState('')

    return (
        <>
            <div>{state}</div>
            <JapanMap
                onClick={(selectedValue: string) => setState(selectedValue)}
                size='500px'
                mapColor='white'
                strokeColor='#4f4f4f'
                strokeWidth='1'
                hoverColor='#3d3d3d'
            />
        </>
    )
}
```

## Props Available

| Props       | Description                                             | Requirement | Default Value |
|-------------|---------------------------------------------------------|-------------|---------------|
| onClick     | Callback function to get the selected state value.      | Required    | NA            |
| className   | Custom classname for the map component.                 | Optional    | "svgmap"      |
| size        | Width of the map.                                       | Optional    | "inherit"     |
| mapColor    | Color of the map.                                       | Optional    | "#ffffff"     |
| strokeColor | Border color of each state.                             | Optional    | "#000000"     |
| strokeWidth | Border width of each state.                             | Optional    | "0.5"         |
| hoverColor  | Color of the state while hovering on it.                | Optional    | "#303030"     |


## Contributing

Pull requests are welcome.

## Credits

Reference of SVG map taken from [MAPSVG](https://mapsvg.com/maps).