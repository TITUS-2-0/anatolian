

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
          ab (@type=rtl-line-wrapper, @xml:id) (multiple)
            choice (multiple)
              reg (@type=transliteration) (multiple)
              orig (@rend=rtl) (multiple)
            [lb (@n) (multiple)]
      div (@data-level=2, @n, @type=text, @xml:id)
        head (@xml:lang=eng-Latn)
        ab (@type=rtl-line-wrapper, @xml:id) (multiple)
          choice (multiple)
            reg (@type=transliteration, @xml:lang=xld-Latn-x-tld) (multiple)
            orig (@rend=rtl) (multiple)
          [lb (@n) (multiple)]
      [note (@xml:id, @xml:lang=eng-Latn)]
        placeName (@xml:id)
    div (@data-level=1, @n, @type=inscription, @xml:id) (multiple)
      ab (@type=rtl-line-wrapper, @xml:id) (multiple)
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
						<ab type="rtl-line-wrapper" xml:id="inscription-1-text-1-ab-2">
							<lb n="A1"/>
							<choice>
								<reg type="transliteration">B 5 L-MRḤŠWN ŠNT 10 ՚RTḤŠSŠ MLK՚</reg>
								<orig rend="rtl">𐡁 5 𐡋-𐡌𐡓𐡇𐡔𐡅𐡍 𐡔𐡍𐡕 10 𐡀𐡓𐡕𐡇𐡔𐡎𐡔 𐡌𐡋𐡊𐡀</orig>
  ...
```
