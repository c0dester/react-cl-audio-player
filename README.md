# react-cl-audio-player

## Repo is forked from [cezarlz](https://github.com/cezarlz)

A simple audio player with ReactJS and CSS3.

Inspiration: [Thanks Rovane Durso](https://dribbble.com/shots/998479-Music)

## TODO

* ~~shuffle~~
* ~~mute/unmute~~
* ~~repeat song~~
* ~~cover~~
* ~~play/pause song~~
* ~~prev/next song~~
* Drag n Drop of the songs
* Better volume control
* List of the songs
* Drag of the progress bar


## Demo & Examples

Live demo: http://cezarlz.github.io/react-cl-audio-player/

To run it on your local environment:

```
yarn install
yarn start
yarn build // to build
```

Then open [`localhost:3000`](http://localhost:3000).


## Installation

```
npm install react-cl-audio-player --save
```


## Usage

```javascript
import AudioPlayer from 'react-cl-audio-player';

<AudioPlayer
  songs={songs}
  autoplay
/>
```

### Properties

```javascript
propTypes = {
  songs: PropTypes.array.isRequired,
  autoplay: PropTypes.bool,
  onTimeUpdate: PropTypes.func,
  onEnded: PropTypes.func,
  onError: PropTypes.func,
  onPlay: PropTypes.func,
  onPause: PropTypes.func,
  onPrevious: PropTypes.func,
  onNext: PropTypes.func,
};
```

Songs model:

```javascript
const songs = [
  {
    url: 'path/to/mp3',
    cover: 'path/to/jpeg',
    artist: {
      name: 'Metallica',
      song: 'Fuel'
    }
  },
  {
    url: 'path/to/your/mp3',
    artist: {
      name: 'X Japan',
      song: 'Art of Life'
    }
  }
];

// Then call
<CLAudioPlayer
  songs={songs}
  autoplay
/>
```

#### CSS classes
* .no-height - A helper class for songs without covers
* .player-container
* .player-cover
* .artist-info
* .artist-name
* .artist-song-name
* .player-progress-container
* .player-progress-value
* .player-options
* .player-buttons
* .player-btn
* .player-btn i (.fa .fa-play .fa-pause .fa-volume .fa-volume-off .fa-forward .fa-backward .fa-repeat .fa-random)
* .player-btn.big.medium.small.active.volume:disabled
* .player-controls

### Notes

Works perfectly in Chrome, Firefox and Safari. No tested in IE.

Version 2.0 was rewritten. Be careful.

## Fork changes:

* List of available songs with play button
* Remove event listeners when component unmounts
* Pause player on unmount to prevent music play when redirect using react router

## License

MIT License.

Copyright (c) 2017 Cezar Luiz.
