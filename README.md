# EXT\_texture\_video

## Contributors

* Takahiro Aoyagi, Mozilla, [@takahirox](https://github.com/takahirox)

## Status

Draft

## Dependencies

Written against the glTF 2.0 spec.

## Overview

T.B.D.

## Example screenshot

T.B.D.

## Defining Videos

```
"extensions": {
    "EXT_texture_video": {
        "videos": [
            {
                "uri": "texture.mp4"
            },
            {
                "bufferView": 0,
                "mimeType": "video/mp4" 
            }
        ]
    }
}
```

## Defining Video textures

```
"textures": [
    {
        "source": 0, // index in images as fallback
        "extensions": {
            "EXT_texture_video": {
                "source": 0 // index in videos
            }
        }
    }
]
```

## Fallback

T.B.D.

## Video Texture Types

| Property | Type | Description | Requires |
|:------|:------|:------|:------|
| `uri` | `string` | | |
| `bufferView` | `integer` | | |
| `mimeType` | `string` | | |
