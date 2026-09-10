# nowrun player — strings

Locale file: `fe/locales/en/common.json`. Keys with an `App` suffix are used when
`isNonGameApp` is true; set the plain key to the same value so both paths match.

## Launching
| key | value |
|---|---|
| `launchStarting` (new) | Starting |
| `launchConnecting` (new) | Connecting |
| `launchQueued` (new) | {{position}} ahead of you |

## Idle check
| key | value |
|---|---|
| `areYouThere` | Are you still there? |
| `idleScreentext` | This app closes after a while with no one using it. Your progress is saved. |
| `stoppingApp` / `stoppingGame` | Closing in {{seconds}}s |
| `iAmStillHere` | Keep going |

## Session ended (all five types share the heading; one body line each)
| key | value |
|---|---|
| `completeHead` / `completeHeadApp` | That's the end of this session |
| `completeMsg` / `completeMsgApp` | Sessions run for a set time. Start a new one and pick up where you left off. |
| `duplicateHead` / `duplicateHeadApp` | That's the end of this session |
| `duplicateMsg` / `duplicateMsgApp` | Someone opened this app in another tab. |
| `migratedHead` / `migratedHeadApp` | That's the end of this session |
| `migratedMsg` / `migratedMsgApp` | This app is open on another device. |
| `inactiveHead` / `inactiveHeadApp` | That's the end of this session |
| `inactiveMsg` / `inactiveMsgApp` | It closed after a while with no one using it. |
| `disconnectedHead` / `disconnectedHeadApp` | That's the end of this session |
| `disconnectedMsg` / `disconnectedMsgApp` | The connection was lost. |
| `restart`, `continuePlayingHere` / `continuePlayingHereApp` | Start a new session |
| `endScreenHeading` / `endScreenHeadingApp` (full-screen exit) | That's the end of this session |
| `endScreenSubHeading` / `endScreenSubHeadingApp` | Sessions run for a set time. Start a new one and pick up where you left off. |
| `restartSession` | Start a new session |

## Server busy
| key | value |
|---|---|
| `serverBusy` | Your app was interrupted |
| `serverBusyMsg` | The cloud device it was running on went away. Starting again takes a few seconds. |
| `restart` | Start again |
| `reportIssue` | Report a problem |

## App crashed
| key | value |
|---|---|
| `appcrash` | The app crashed |
| body (new key, e.g. `appcrashBody`) | It closed unexpectedly. You can start it again. |
| `crashType` | keep; rendered as the small mono line, value unchanged |

## Connection lost
| key | value |
|---|---|
| `reconnecting` | Reconnecting |
| `spotInstanceShortMsg` | Reconnecting |
| `slowInternetConnection` | Slow connection |

## Wallpaper
No strings. Asset only: `wallpaper-dark.png` as the default `media.desktop.banner` / `media.mobile.banner`
in `ncm/src/ncmConstants.ts`. A per-app studio `game-wallpaper` still overrides it. `wallpaper-light.png` is
there if the 70% overlay in `components/wrapper` is ever removed; with the overlay it goes grey.

## Generic popup
One component for every in-session message: title, one line, up to two actions. Per use, four strings.
| slot | rule | example on the page |
|---|---|---|
| title | a short question or statement | Leave this app? |
| body | one line: what happens, what is kept | Your progress is saved. You can come back to it. |
| primary | the safe verb | Stay |
| secondary | the other verb | Leave |

## Location permission
| key | value |
|---|---|
| `permission` (single, known permission) | This app uses your location |
| `permission` (more than one, or unknown) | This app needs your permission |
| body (new key, e.g. `permissionBody`) | Your browser will ask you next. nowrun passes it to the app. |
| permission names (kept, shown as the mono line) | Location · Microphone · Camera · Files |
| `gotIt` | Continue |
| `cancel` | Not now |
