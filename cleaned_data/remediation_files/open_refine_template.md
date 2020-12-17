# Open Refine Template for WPA\TVA


## Template

#### Prefix

```
<?xml version="1.0" encoding="UTF-8"?>
<modsCollection xmlns="http://www.loc.gov/mods/v3" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xlink="http://www.w3.org/1999/xlink" xsi:schemaLocation="http://www.loc.gov/mods/v3 http://www.loc.gov/standards/mods/v3/mods-3-5.xsd">
```
####Body

```
<mods>
{{if(isBlank(cells['identifier'].value), '', '<identifier type="local">' + cells['identifier'].value + '</identifier>')}}
{{if(isBlank(cells['wpa:photograph_number'].value), '', '<identifier>' + cells['wpa:photograph_number'].value + '</identifier>')}}
<titleInfo><title>{{cells['title'].value}}</title></titleInfo>
{{if(isBlank(cells['abstract'].value), '', '<abstract>' + cells['abstract'].value + '</abstract>')}}
<physicalDescription><form authority="aat" valueURI="http://vocab.getty.edu/aat/300046300">photographs</form></physicalDescription>

{{if(isBlank(cells['creator 1'].value), '', '<name><namePart>' + cells['creator 1'].value + '</namePart><role>
<roleTerm type="text" authority="marcrelator" valueURI="http://id.loc.gov/vocabulary/relators/ctb">Contributor</roleTerm></role></name>')}}
{{if(isBlank(cells['creator 2'].value), '', '<name><namePart>' + cells['creator 2'].value + '</namePart><role>
<roleTerm type="text" authority="marcrelator" valueURI="http://id.loc.gov/vocabulary/relators/ctb">Contributor</roleTerm></role></name>')}}
{{if(isBlank(cells['creator 3'].value), '', '<name><namePart>' + cells['creator 3'].value + '</namePart><role>
<roleTerm type="text" authority="marcrelator" valueURI="http://id.loc.gov/vocabulary/relators/ctb">Contributor</roleTerm></role></name>')}}
{{if(isBlank(cells['creator 4'].value), '', '<name><namePart>' + cells['creator 4'].value + '</namePart><role>
<roleTerm type="text" authority="marcrelator" valueURI="http://id.loc.gov/vocabulary/relators/ctb">Contributor</roleTerm></role></name>')}}
{{if(isBlank(cells['observer'].value), '', '<name><namePart>' + cells['observer'].value + '</namePart><role>
<roleTerm type="text" authority="marcrelator" valueURI="http://id.loc.gov/vocabulary/relators/wit">Witness</roleTerm></role></name>')}}
{{if(isBlank(cells['observer2'].value), '', '<name><namePart>' + cells['observer2'].value + '</namePart><role>
<roleTerm type="text" authority="marcrelator" valueURI="http://id.loc.gov/vocabulary/relators/wit">Witness</roleTerm></role></name>')}}
{{if(isBlank(cells['observer3'].value), '', '<name><namePart>' + cells['observer3'].value + '</namePart><role>
<roleTerm type="text" authority="marcrelator" valueURI="http://id.loc.gov/vocabulary/relators/wit">Witness</roleTerm></role></name>')}}
{{if(isBlank(cells['date_text'].value), '', '<originInfo><dateCreated>' + cells['date_text'].value + '</dateCreated><dateCreated encoding="edtf" keyDate="yes">' + cells['date_edtf'].value + '</dateCreated></originInfo>')}}

{{if(isBlank(cells['note'].value), '', '<note>' + cells['note'].value + '</note>')}}
{{if(isBlank(cells['wpa:feature_number'].value), '', '<note>' + cells['wpa:feature_number'].value + '</note>')}}
{{if(isBlank(cells['wpa:field_specimen'].value), '', '<note>' + cells['wpa:field_specimen'].value + '</note>')}}
{{if(isBlank(cells['burial_number'].value), '', '<note>' + cells['burial_number'].value + '</note>')}}

{{if(isBlank(cells['subject'].value), '', '<subject' + if(isBlank(cells['subject_URI'].value), '', ' authority="lcsh" valueURI="' + cells['subject_URI'].value + '"') + '><topic>' + cells['subject'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject2'].value), '', '<subject' + if(isBlank(cells['subject2_URI'].value), '', ' authority="lcsh" valueURI="' + cells['subject2_URI'].value + '"') + '><topic>' + cells['subject2'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject3'].value), '', '<subject' + if(isBlank(cells['subject3_URI'].value), '', ' authority="lcsh" valueURI="' + cells['subject3_URI'].value + '"') + '><topic>' + cells['subject3'].value + '</topic></subject>')}}
{{if(isBlank(cells['photocategory'].value), '', '<subject' + if(isBlank(cells['photocategory_URI'].value), '', ' authority="lcsh" valueURI="' + cells['photocategory_URI'].value + '"') + '><topic>' + cells['photocategory'].value + '</topic></subject>')}}
{{if(isBlank(cells['photocategory2'].value), '', '<subject' + if(isBlank(cells['photocategory2_URI'].value), '', ' authority="lcsh" valueURI="' + cells['photocategory2_URI'].value + '"') + '><topic>' + cells['photocategory2'].value + '</topic></subject>')}}
{{if(isBlank(cells['photocategory3'].value), '', '<subject' + if(isBlank(cells['photocategory3_URI'].value), '', ' authority="lcsh" valueURI="' + cells['photocategory3_URI'].value + '"') + '><topic>' + cells['photocategory3'].value + '</topic></subject>')}}
{{if(isBlank(cells['photocategory4'].value), '', '<subject' + if(isBlank(cells['photocategory4_URI'].value), '', ' authority="lcsh" valueURI="' + cells['photocategory4_URI'].value + '"') + '><topic>' + cells['photocategory4'].value + '</topic></subject>')}}
{{if(isBlank(cells['photocategory5'].value), '', '<subject' + if(isBlank(cells['photocategory5_URI'].value), '', ' authority="lcsh" valueURI="' + cells['photocategory5_URI'].value + '"') + '><topic>' + cells['photocategory5'].value + '</topic></subject>')}}

{{if(isBlank(cells['subject_temporal'].value), '', '<subject><temporal>' + cells['subject_temporal'].value + '</temporal></subject>')}}
{{if(isBlank(cells['subject_temporal2'].value), '', '<subject><temporal>' + cells['subject_temporal2'].value + '</temporal></subject>')}}
{{if(isBlank(cells['subject_temporal3'].value), '', '<subject><temporal>' + cells['subject_temporal3'].value + '</temporal></subject>')}}
{{if(isBlank(cells['date_subject_temporal'].value), '', '<subject><temporal encoding="edtf">' + cells['date_subject_temporal'].value + '</temporal></subject>')}}
{{if(isBlank(cells['date_subject_temporal 1'].value), '', '<subject><temporal encoding="edtf" point="start">' + cells['date_subject_temporal 1'].value + '</temporal></subject><subject><temporal encoding="edtf" point="end">' + cells['date_subject_temporal 2'].value + '</temporal></subject>')}}

{{if(isBlank(cells['subject_name'].value), '', '<subject' + if(isBlank(cells['subject_name_URI'].value), '', ' authority="naf" valueURI="' + cells['subject_name_URI'].value + '"') + '><name><namePart>' + cells['subject_name'].value + '</namePart></name></subject>')}}
{{if(isBlank(cells['subject_name2'].value), '', '<subject' + if(isBlank(cells['subject_name2_URI'].value), '', ' authority="naf" valueURI="' + cells['subject_name2_URI'].value + '"') + '><name><namePart>' + cells['subject_name2'].value + '</namePart></name></subject>')}}
{{if(isBlank(cells['subject_name3'].value), '', '<subject' + if(isBlank(cells['subject_name3_URI'].value), '', ' authority="naf" valueURI="' + cells['subject_name3_URI'].value + '"') + '><name><namePart>' + cells['subject_name3'].value + '</namePart></name></subject>')}}
{{if(isBlank(cells['subject_name4'].value), '', '<subject' + if(isBlank(cells['subject_name4_URI'].value), '', ' authority="naf" valueURI="' + cells['subject_name4_URI'].value + '"') + '><name><namePart>' + cells['subject_name4'].value + '</namePart></name></subject>')}}

{{if(isBlank(cells['wpa:county'].value), '', '<subject authority="naf" valueURI="' + cells['wpa:county_URI'].value + '"><geographic>' + cells['wpa:county'].value + '</geographic></subject>')}}
{{if(isBlank(cells['subject_geo'].value), '', '<subject authority="lcsh" valueURI="' + cells['subject_geo_URI'].value + '"><geographic>' + cells['subject_geo'].value + '</geographic></subject>')}}
{{if(isBlank(cells['subject_geo2'].value), '', '<subject><geographic>' + cells['subject_geo2'].value + '</geographic></subject>')}}
{{if(isBlank(cells['subject_geo3'].value), '', '<subject authority="naf" valueURI="' + cells['subject_geo3'].value + '"><geographic>' + cells['subject_geo3'].value + '</geographic></subject>')}}


<typeOfResource>still image</typeOfResource>
<relatedItem displayLabel="Project" type="host"><titleInfo><title>WPA/TVA Archeological Photographs</title></titleInfo></relatedItem>
{{if(isBlank(cells['project_name'].value), '', '<relatedItem displayLabel="Collection" type="host"><titleInfo><title>' + cells['project_name'].value + '</title></titleInfo></relatedItem>')}}
<recordInfo><recordContentSource valueURI="{{cells['recordSource_URI'].value}}">{{cells['recordSource'].value}}</recordContentSource></recordInfo>
<accessCondition type="use and reproduction" xlink:href="{{cells['rights_URI'].value}}">{{cells['rights'].value}}</accessCondition>
</mods>

```

#### Suffix

```
</modsCollection>
```