# Fluence NFTs User Guide

The Fluence NFTs are 3D environments created in Blender 2.8.

The blend files are located in the [Blend Files Folder](https://github.com/ben-razor/fluence-artwork/tree/main/blend)

## Configuration

To configure the different styles and items in the scene. NFT metadata can be loaded into the blend files.

The metadata is slightly different depending on the type of scene (investor, developer, community). Here are
example metadata files:

### Investor

```json
{
    "type": "investor",
    "topology": "mesh",
    "NetworkRing": "Gold",
    "NetworkStar": "Gold",
    "Logo": "Gold",
    "LogoGem": "flubie",
    "Surface": "cloth_silk",
    "SurfaceNetwork": "network_gold",
    "logo_gems": [
        {"type": "LogoDiamondRingCross", "material": "Gold"},
        {"type": "LogoDiamondRingDiag", "material": "Gold"},
        {"type": "LogoDiamondBar", "material": "Gold"}
    ],
    "front": {
        "type": "Coin",
        "material": "Silver"
    },
    "side": {
        "type": "Crystal",
        "color": "onyx"
    },
    "back": {
        "type": "Flubie",
        "color": "flubie"
    }
}
```

### Developer
```json
{
    "type": "dev",
    "topology": "mesh",
    "NetworkRing": "PinkLED",
    "NetworkStar": "FiberOptic",
    "Surface": "cloth_dev_blue",
    "SurfaceNetwork": "fluroviola",
    "logo_gems": [
        {"type": "LogoDiamondRingCross", "material": "GreenLED"},
    ],
    "front": {
        "type": "Aquafish",
        "color": "flurofluence"
    },
    "side": {
        "type": "Flugelhog",
        "color": "hoghog",
    },
    "back": {
        "type": "Coral",
        "color": "coralfluence",
        "pearl_color": "glowpearl"
    }
}
```

### Community 
```json
{
    "type": "nature",
    "topology": "mesh",
    "NetworkRing": "Silver",
    "NetworkStar": "FiberOptic",
    "Surface": "cloth_earth",
    "SurfaceNetwork": "network_gold",
    "front": {
        "type": "FlibertyCap",
        "material": "Gold"
    },
    "side": {
        "type": "FluAgaric",
        "color": "fluagaric_fluence",
    },
    "back": {
        "type": "Neuron",
        "color": "neuron_fluence"
    }
}
```

## Schema

This schema contains the styles options and styles available for each type of scene.

```json
{
    "topologies": ["ring", "star", "mesh"],
    "investor": {
        "type": "investor",
        "network": {
            "type": "material",
            "options": ["Gold", "Silver", "Flumium", "FiberOptic"]
        },
        "logo": {
            "Logo": {
                "type": "material",
                "options": ["Gold", "Silver", "Flumium"]
            },
            "LogoGem": {
                "type": "color",
                "options": ["diamond", "flubie", "emerald"]
            }
        },
        "logo_gems": {
            "LogoDiamondRingCross": {
                "type": "material",
                "options": ["Gold", "Silver", "Flumium"]
            },
            "LogoDiamondRingDiag": {
                "type": "material",
                "options": ["Gold", "Silver", "Flumium"]
            },
            "LogoDiamondBar": {
                "type": "material",
                "options": ["Gold", "Silver", "Flumium"]
            }
        },
        "surface": {
            "Surface": {
                "type": "color",
                "options": ["cloth_fluence", "cloth_gold", "cloth_silk"]
            },
            "SurfaceNetwork": {
                "type": "color",
                "options": ["flurofluence", "flurogreen", "fluroviola", "fluroaqua"]
            }
        },
        "items": {
            "Flubie": {
                "type": "color",
                "options": ["diamond", "flubie", "emerald"]
            },
            "Crystal": {
                "type": "color",
                "options": ["diamond", "flubie", "emerald", "onyx"]
            },
            "Coin": {
                "type": "material",
                "options": ["Gold", "Silver", "Flumium"]
            }
        }
    },
    "dev": {
        "type": "dev",
        "network": {
            "type": "material",
            "options": ["PinkLED", "GreenLED", "BlueLED", "FiberOptic"]
        },
        "logo": {
            "Logo": {
                "type": "color",
                "options": ["Fluicon"]
            },
            "LogoGem": {
                "type": "color",
                "options": ["diamond", "flubie", "emerald"]
            }
        },
        "logo_gems": {
            "LogoDiamondRingCross": {
                "type": "color",
                "options": ["PinkLED", "GreenLED", "BlueLED"]
            }
        },
        "surface": {
            "Surface": {
                "type": "color",
                "options": ["cloth_dev_fluence", "cloth_dev_silver", "cloth_dev_blue"]
            },
            "SurfaceNetwork": {
                "type": "color",
                "options": ["network_fluence", "network_dark", "network_aqua"]
            }
        },
        "items": {
            "Aquafish": {
                "type": "color",
                "options": ["flurofluence", "flurogreen", "fluroviola", "fluroaqua"]
            },
            "Airhead": {
                "type": "color",
                "options": ["airhead", "airslimy", "airsuit"]
            },
            "Flugelhog": {
                "type": "color",
                "options": ["hoghog", "hogbrown", "hogyellow"]
            },
            "Coral": {
                "type": "color",
                "options": ["coralfluence", "coralblue", "coraldark"]
            },
            "Pearl": {
                "type": "color",
                "options": ["glowfluence", "glowyellow", "glowpearl"],
                "extra_to": "Coral"
            }
        }
    },
    "community": {
        "type": "community",
        "network": {
            "type": "material",
            "options": ["Gold", "Silver", "Flumium", "FiberOptic"]
        },
        "logo": {
            "Logo": {
                "type": "material",
                "options": ["Gold", "Silver", "Flumium"]
            }
        },
        "surface": {
            "Surface": {
                "type": "color",
                "options": ["cloth_cerebrum", "cloth_earth", "cloth_psy", "cloth_awakening"]
            },
            "SurfaceNetwork": {
                "type": "color",
                "options": ["network_fluence", "network_gold", "network_chlorophyll"]
            }
        },
        "items": {
            "FlibertyCap": {
                "type": "material",
                "options": ["Gold", "Silver", "Flumium", "FiberOptic"]
            },
            "FluAgaric": {
                "type": "color",
                "options": ["fluagaric_fluence", "fluagaric_aqua", "fluagaric_purple"]
            },
            "Neuron": {
                "type": "color",
                "options": ["neuron_fluence", "neuron_aqua", "neuron_clean"]
            }
        }
    }
}
```