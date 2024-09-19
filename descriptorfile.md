## Columns

### First Generation Descriptors

The column names for Gen 1 descriptors follow the format:

`{material class}_{math type}_{descriptor name}`

where:
- **`material class`**: metal, metalloid, nonmetal 
- **`math type`**:
  - `mean`: mean value of the descriptor properties among elemental species
  - `min`: min value of the descriptor properties among elemental species
  - `max`: max value of the descriptor properties among elemental species
  - `cuml`: cumulative mean value taking into account the atom number
- **`descriptor name`**: name of the descriptor property (refer to Table 1)

Consider the example of H₂O:
In H₂O, there are two Hydrogen atoms and one Oxygen atom. So, the total elemental species are two (H and O), and the total number of atoms is 3.

For mean, min, and max:<br>
<pre>
- min = min(at. number of H, at. number of O) = 1
- max = max(at. number of H, at. number of O) = 8
- mean = mean(at. number of H, at. number of O) = 4.5
</pre>

For cumulative values, we consider the number of atoms: <br>
<pre>
- cuml = (at. number of H × number of H atoms + at. number of O × number of O atoms) / total number of atoms
  - = (1 × 2 + 8 × 1) / 3 = 5 <br>
</pre>

### First Generation Descriptors Table

| Descriptor Name                          | Description                                                       |
|------------------------------------------|-------------------------------------------------------------------|
| `{material class}_mean_{descriptor name}`   | Mean value of the descriptor properties among elemental species |
| `{material class}_min_{descriptor name}`     | Min value of the descriptor properties among elemental species  |
| `{material class}_max_{descriptor name}`     | Max value of the descriptor properties among elemental species  |
| `{material class}_cuml_{descriptor name}`    | Cumulative mean value considering the atom number                |

*Table 1*: _**Descriptors with Prefixes** `{material class}_{math type}_{descriptor name}`_

| Descriptor Name | Description                                           |
|-----------------|-------------------------------------------------------|
| `at_mass_no`    | Atomic mass number                                   |
| `at_radius`     | Atomic radius                                        |
| `at_wt`         | Atomic weight                                        |
| `atomic_no`     | Atomic number                                        |
| `ionization_en` | Ionization energy                                    |
| `neutron_no`    | Number of neutrons                                   |
| `oxi_no`        | Oxidation number                                     |
| `pauling_en`    | Pauling electronegativity                            |
| `period`        | Period of the element                                |
| `valence`       | Valence electrons of the element                     |
| `vdw_radius`    | van der Waals radius                                 |

*Table 2*: _**Descriptors without Prefixes**_

| Descriptor Name                    | Description                                                      |
|------------------------------------|------------------------------------------------------------------|
| `sum_atwt_m_sm`                    | Sum of atomic weight of metals and metalloids                    |
| `sum_electron_m_sm`                | Sum of atomic numbers of metals and metalloids                   |
| `sum_m_sm`                         | Summation of the number of metals and metalloids                 |
| `sum_mass_no_m_sm`                 | Sum of mass numbers of metals and metalloids                     |
| `sum_neutron_no_m_sm`              | Sum of neutron numbers of metals and metalloids                  |
| `total_atoms`                      | Total number of atoms                                           |
| `total_metal_no`                   | Total number of metal atoms                                     |
| `total_metalloids_no`              | Total number of metalloid atoms                                 |
| `total_mw`                         | Total molecular weight                                          |
| `total_non_metal_no`               | Total number of non-metal atoms                                 |
| `total_nonmetal_hetero_no`         | Total number of non-metallic heteroatoms (N, O, F, P, S, Cl, Se, Br, I, At) excluding hydrogen |
| `total_oxy_atoms_no`               | Total number of oxygen atoms                                    |

### Second Generation Descriptors

Second generation descriptors use cumulative values and are classified into two categories:

| Descriptor Name            | Description                                                                        |
|----------------------------|------------------------------------------------------------------------------------|
| `lambda`                   | (Atomic number of metal - Valence electrons of metal) / Valence electrons of metal |
| `mu`                       | 1 / (period of metal)                                                              |
| `alpha_metal`             | lambda × mu                                                                        |
| `total_alpha_metal`       | alpha_metal × Number of metal atoms                                                |
| `alpha_oxy`               | Number of oxygens × 0.33                                                           |
| `total_core`              | alpha_metal + alpha_oxy                                                            |
| `en_metal`                | -alpha_metal + (0.3 × Number of metals)                                            |
| `en_oxygen`               | -alpha_oxy + (0.3 × Valence electrons of oxygen)                                   |
| `total_en`                | en_metal × Number of metals + en_oxygen × Number of oxygens                        |
| `total_en_per_atoms`      | total_en / total number of atoms                                                   |
| `total_en_per_atoms_square`| (total_en_per_atoms)²                                                              |
| `sum_alpha_square`        | total_core²                                                                        |
| `formula`                 | Chemical formula                                                                   |
| `smiles`                  | SMILES notation                                                                    |

*Table 3*: _**Second Generation Descriptors**_
