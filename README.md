# Tumor/Stroma classification using Random Decision Forests

Cells are classified into *tumor* or *stroma* classes based on antigen expression levels of each cell.  Data from 31 different antigens are organized as follows:

| CCR3 | CD103 | ... | Class |
| ---: | ---: | :---: | :--- |
| 0.115 | 0.217 | ... | stroma |
| 1.216 | 0.412 | ... | stroma |
| 0.662 | 0.326 | ... | tumor |

The following antigens are available:

`['CCR3', 'CD103', 'CD11B', 'CD141', 'CD163', 'CD19', 'CD3', 'CD31', 'CD4', 'CD45RA', 'CD56', 'CD62L', 'CD8', 'CXCR3', 'EPCAM', 'FAP', 'FOXP3', 'GFAP', 'GZMB', 'IL10', 'INOS', 'KI67', 'LOX1', 'TRYPTASE', 'MPO', 'MUC1', 'PD1', 'PDL1', 'PRG2', 'SMA', 'VIMENTIN']`

A total of 268074 cells were identified from 6 patients on multiplexed whole slide images.  Regions were identified as `tumor` or `stroma` by pathologists.  Fitting random forest models, antigens are ranked per feature importance as reported by the best models.  The scripts analyze the following tests on `all patients` and `individual patients`:

- `all antigens`
- `all antigens but MUC1, KI67, EPCAM`
- `all but top K antigens by intensity means`
- `only top K antigens found after ranking all antigens`


## 👥 Contributing

Within the Informatics Center, we value the health of our community as much as we do code. As a result, we ask you read through the following:

-   Our [contributor's guide](https://github.com/EDRN/.github/blob/main/CONTRIBUTING.md) tells what kinds of contributions we take.
-   Our [code of conduct](https://github.com/EDRN/.github/blob/main/CODE_OF_CONDUCT.md) delineates the standards of behavior we both practice and expect by everyone who participates with this software.


### 🔢 Versioning

At present, only the source code and its data are being made public.


## 📃 License

The project is licensed under the [Apache version 2](LICENSE.md) license.
