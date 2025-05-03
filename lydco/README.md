# Dataset 'Corpus of Lydian Inscriptions'

![Static Badge](https://img.shields.io/badge/TEI_validation-passing-green)

This is a TEI port of a [TITUS dataset](http://titus.uni-frankfurt.de/texte/etcs/anatol/lydian/lydco.htm).

* URL: https://titus2.uni-frankfurt.de/dataset/lydco
* version: 0.1.0
* date: 2025-04-23

## Citation
```text
Digital version of Corpus of Lydian Inscriptions (v0.1.0). By: Jost Gippert, Florian Matter, H.C. Melchert, J. Tischler. In: Carling, Gerd & Jost Gippert (2025). TITUS 2.0. Frankfurt: Goethe University. (URL: https://titus2.uni-frankfurt.de/dataset/lydco, visited on <insert date>)
```

## TEI encoding


### Unit Mapping
The TITUS 1 structural units are mapped onto TEI as follows:

| Source Unit | TEI Mapping | Notes |
|-------------|-------------|-------|
| Inscription | `div@inscription` | Automatically translated into named div |
| Line | `lb` |  |

### Structural overview
```text
text (@xml:lang=xld-Lydi)
  body
    div (@data-level=1, @n, @type=inscription, @xml:id)
      div (@data-level=2, @n, @type=text, @xml:id, @xml:lang=arc-Latn-x-tld)
        head (@xml:lang=eng-Latn)
        ab (@xml:id)
          ab (@type=line-wrapper, @xml:id) (multiple)
            choice (multiple)
              reg (@type=transliteration) (multiple)
              orig (@rend=rtl) (multiple)
            [lb (@n) (multiple)]
      div (@data-level=2, @n, @type=text, @xml:id)
        head (@xml:lang=eng-Latn)
        ab (@type=line-wrapper, @xml:id) (multiple)
          choice (multiple)
            reg (@type=transliteration, @xml:lang=xld-Latn-x-tld) (multiple)
            orig (@rend=rtl) (multiple)
          [lb (@n) (multiple)]
      [note (@xml:id, @xml:lang=eng-Latn)]
        placeName (@xml:id)
    div (@data-level=1, @n, @type=inscription, @xml:id) (multiple)
      ab (@type=line-wrapper, @xml:id) (multiple)
        choice (multiple)
          reg (@type=transliteration, @xml:lang=xld-Latn-x-tld) (multiple)
          orig (@rend=rtl) (multiple)
        [lb (@n) (multiple)]
      [note (@xml:id, @xml:lang=eng-Latn) (multiple)]
        placeName (@xml:id) (multiple)
```

### Structure Example

```xml
<div xmlns="http://www.tei-c.org/ns/1.0" n="1" xml:id="inscription-1" type="inscription" data-level="1">
				<note xml:id="inscription-1-note-1" xml:lang="eng-Latn">
					<placeName xml:id="inscription-1-note-1-placeName-1">Sardes</placeName>
				</note>
				<div n="1a" xml:id="inscription-1-text-1" type="text" data-level="2" xml:lang="arc-Latn-x-tld">
					<head xml:lang="eng-Latn">Aramaic inscription</head>
					<ab xml:id="inscription-1-text-1-ab-1">
						<ab type="line-wrapper" xml:id="inscription-1-text-1-ab-2">
							<lb n="A1"/>
							<choice>
								<reg type="transliteration">B 5 L-MRḤŠWN ŠNT 10 ՚RTḤŠSŠ MLK՚</reg>
								<orig rend="rtl">𐡁 5 𐡋-𐡌𐡓𐡇𐡔𐡅𐡍 𐡔𐡍𐡕 10 𐡀𐡓𐡕𐡇𐡔𐡎𐡔 𐡌𐡋𐡊𐡀</orig>
  ...
```
