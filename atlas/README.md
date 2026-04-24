# ENIGMA Symmetric White Matter Tractography Atlas

## Overview

![ENIGMA Symmetric White Matter Tractography Atlas](ENIGMA_atlas_figure.jpg)

The ENIGMA Symmetric White Matter Tractography Atlas is a population-averaged tractography atlas comprising 65 white matter bundles, designed for large-scale diffusion MRI studies. The atlas was constructed from the HCP-1065 template [1] by combining bilateral bundles and applying the minimum direct flip distance (MDF) metric [2] to enforce uniform streamline density, thereby minimizing hemispheric asymmetry and reducing analytical biases arising from anatomical differences between the left and right hemispheres.
To achieve anatomically and functionally interpretable bundles, several tracts were redefined based on their cortical termination points. The thalamic radiation and corticostriatal tract were combined and then subdivided by the central sulcus. Similarly, the corticopontine tract and corpus callosum body were divided by the central sulcus. The final atlas encompasses 65 bundles across four white matter systems: 34 association, 16 projection (basal ganglia), 10 projection (brainstem), and 5 commissural tracts.

### Atlas Versions
| Version    | MDF Threshold | Description                                                       |
|------------|---------------|-------------------------------------------------------------------|
| **Full**   | 0.5 mm        | Uniform streamline density
| **Sparse** | 1–2.5 mm        | Reduced streamline density and optimized for computational efficiency in DSI-Studio |

### Directory Structure
```
ENIGMA_atlas/
├── README.md
├── MNI152_2mm/
│   ├── Full/
        ├── tt_gz/
        └── trk/
│   └── Sparse/
        ├── tt_gz/
        └── trk/
└── MNI152_1mm/
    ├── Full/
        ├── tt_gz/
        └── trk/
    └── Sparse/
        ├── tt_gz/
        └── trk/
```
---

### Atlas Spaces
| Folder       | Resolution   | Template                              |
|--------------|--------------|---------------------------------------|
| `MNI152_2mm` | 2 mm isotropic | ICBM152 2009a space                 |
| `MNI152_1mm` | 1 mm isotropic | `mni_icbm152_t1_tal_nlin_asym_09a`  |

### References
1. F.-C. Yeh, "Population-based tract-to-region connectome of the human brain and its hierarchical topology," *Nat. Commun.*, vol. 13, no. 1, pp. 1–13, Aug. 2022.
2. E. Garyfallidis, M. Brett, M. M. Correia, G. B. Williams, and I. Nimmo-Smith, "QuickBundles, a Method for Tractography Simplification," *Front. Neurosci.*, vol. 6, p. 175, Dec. 2012.
