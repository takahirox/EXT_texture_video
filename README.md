# EXT\_texture\_video

## Contributors

* Takahiro Aoyagi, Mozilla, [@takahirox](https://github.com/takahirox)

## Status

Draft

## Dependencies

Written against the glTF 2.0 spec.

## Overview

The glTF 2.0 core spec allows only PNG and JPEG for texture images.

This `EXT_texture_video` extension allows video as texture sources.
With this extension objects with animated textures can be easily represented in glTF,
ie. TV screen.

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

## Video Types

| Property | Type | Description | Requires |
|:------|:------|:------|:------|
| `uri` | `string` | | No |
| `bufferView` | `integer` | | No |
| `mimeType` | `string` | | No |

## Video Texture Types

T.B.D.
