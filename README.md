<?xml version="1.0" encoding="utf-8"?>
<style xmlns="http://purl.org/net/xbiblio/csl" version="1.0" class="in-text">
  <info>
    <title>Guía PUCP</title>
    <id>https://s3.amazonaws.com/files.pucp.edu.pe/homepucp/uploads/2016/06/08105745/Guia_PUCP_para_el_registro_y_citado_de_fuentes-2015.pdf</id>
    <author>
      <name>Equipo de la Guía PUCP</name>
      <email>example@pucp.edu.pe</email>
    </author>
    <contributor>
      <name>Miguel Carneiro</name>
    </contributor>
    <contributor>
      <name>Paola Cépeda</name>
    </contributor>
    <contributor>
      <name>Elizabeth Tavera</name>
    </contributor>
    <contributor>
      <name>Héctor Velásquez</name>
    </contributor>
    <contributor>
      <name>Mercedes Mayna</name>
    </contributor>
    <contributor>
      <name>Karem Robertson</name>
    </contributor>
    <contributor>
      <name>Andrea Sato</name>
    </contributor>
    <contributor>
      <name>José Miguel Vidal</name>
    </contributor>
    <category citation-format="author-date"/>
    <updated>2023-03-15T23:15:56+00:00</updated>
    <link href="https://s3.amazonaws.com/files.pucp.edu.pe/homepucp/uploads/2016/06/08105745/Guia_PUCP_para_el_registro_y_citado_de_fuentes-2015.pdf"/>
  </info>
  <locale>
    <terms>
      <term name="anonymous">AUTOR DESCONOCIDO.</term>
      <term name="no date">s/f</term>
      <term name="in">En</term>
      <term name="accessed">Consulta:</term>
      <term name="viewed">Vista:</term>
      <term name="from">En</term>
    </terms>
  </locale>
  <macro name="author/editor">
  <choose>
    <!-- Un autor -->
    <if type="chapter" match="none">
      <names variable="author">
        <name delimiter-precedes-last="never" initialize-with=". " name-as-sort-order="all" sort-separator=", " and="text" delimiter=", ">
          <name-part name="family" text-case="uppercase"/>
          <name-part name="given" text-case="capitalize-first"/>
        </name>
      </names>
      <text>, (<text variable="issued" delimiter=":" suffix="." prefix=" "/><text variable="page"/>).</text>
    </if>
    <!-- Dos autores -->
    <if type="chapter" match="none">
      <names variable="author/editor">
        <name delimiter-precedes-last="never" initialize-with=". " name-as-sort-order="all" sort-separator=", " and="text" delimiter=", ">
          <name-part name="family" text-case="uppercase"/>
          <name-part name="given" text-case="capitalize-first"/>
        </name>
        <name delimiter=", ">
          <name-part name="family" text-case="uppercase"/>
          <name-part name="given" text-case="capitalize-first"/>
        </name>
      </names>
      <text>, (<text variable="issued" delimiter=":" suffix="." prefix=" "/><text variable="page"/>).</text>
    </if>
    <!-- Tres autores -->
    <if type="chapter" match="none">
      <names variable="author/editor">
        <name delimiter-precedes-last="never" initialize-with=". " name-as-sort-order="all" sort-separator=", " and="text" delimiter=", ">
          <name-part name="family" text-case="uppercase"/>
          <name-part name="given" text-case="capitalize-first"/>
        </name>
        <name delimiter=", ">
          <name-part name="family" text-case="uppercase"/>
          <name-part name="given" text-case="capitalize-first"/>
        </name>
        <name delimiter=", " prefix="y ">
          <name-part name="family" text-case="uppercase"/>
          <name-part name="given" text-case="capitalize-first"/>
        </name>
      </names>
      <text>, (<text variable="issued" delimiter=":" suffix="." prefix=" "/><text variable="page"/>).</text>
    </if>
    <!-- Cuatro autores o más -->
    <else>
      <names variable="author/editor" delimiter=", " prefix=". ">
        <name delimiter-precedes-last="never" initialize-with=". " name-as-sort-order="all" sort-separator=", " and="text" delimiter=", ">
          <name-part name="family" text-case="uppercase"/>
          <name-part name="given" text-case="capitalize-first"/>
        </name>
        <substitute>
          <text>otros</text>
        </substitute>
      </names>
      <text>, (<text variable="issued" delimiter=":" suffix="." prefix=" "/><text variable="page"/>).</text>
    </else>
  </choose>
</macro>
  <macro name="editor">
    <names variable="editor">
      <name initialize="true" initialize-with="." and="text" sort-separator=", " delimiter=", " delimiter-precedes-last="never">
        <name-part name="family" text-case="uppercase"/>
        <name-part name="given"/>
      </name>
      <label prefix=" (" form="short" suffix=".)"/>
    </names>
  </macro>
  <macro name="translator">
    <names variable="translator">
      <name and="text" name-as-sort-order="all" sort-separator=", " delimiter=", " delimiter-precedes-last="never">
        <name-part name="family" text-case="uppercase"/>
        <name-part name="given"/>
      </name>
      <label prefix=" (" form="short" suffix=".)"/>
    </names>
  </macro>
  <macro name="author-citation">
    <choose>
      <if variable="author editor translator title title-short" match="any">
        <names variable="author" font-style="normal" font-variant="normal" font-weight="normal">
          <name form="short" and="text" sort-separator=", " name-as-sort-order="all" delimiter=", " delimiter-precedes-last="never"/>
          <substitute>
            <names variable="editor"/>
            <names variable="translator"/>
            <text variable="title-short" prefix="«" suffix="»"/>
            <text variable="title" prefix="«" suffix="»"/>
          </substitute>
        </names>
      </if>
    </choose>
  </macro>
  <macro name="container-author">
    <names variable="container-author">
      <name initialize="true" initialize-with="." and="text" sort-separator=", " delimiter=", " delimiter-precedes-last="never">
        <name-part name="family" text-case="uppercase"/>
        <name-part name="given"/>
      </name>
      <substitute>
        <text macro="editor"/>
        <text macro="translator"/>
        <text variable="note"/>
      </substitute>
    </names>
  </macro>
  <macro name="year-date">
    <choose>
      <if variable="issued">
        <date variable="issued">
          <date-part name="year" form="long"/>
        </date>
      </if>
      <else>
        <text term="no date"/>
      </else>
    </choose>
  </macro>
  <macro name="title">
    <choose>
      <if type="book thesis map motion_picture song manuscript" match="any">
        <text variable="title" font-style="italic"/>
      </if>
      <else-if type="paper-conference speech chapter article-journal article-magazine article-newspaper post-weblog post webpage broadcast entry-dictionary entry-encyclopedia report" match="any">
        <text variable="title" suffix=". "/>
        <choose>
          <if variable="container-author editor note" match="any">
            <text term="in" text-case="capitalize-first" suffix=": "/>
            <text macro="container-author"/>
            <choose>
              <if variable="container-title event" match="any">
                <text value=", "/>
              </if>
            </choose>
          </if>
        </choose>
        <choose>
          <if variable="container-title">
            <text variable="container-title" font-style="italic"/>
          </if>
          <else>
            <text variable="event" font-style="italic"/>
          </else>
        </choose>
      </else-if>
      <else-if type="report">
        <text variable="title" font-style="italic"/>
      </else-if>
      <else-if type="patent">
        <text variable="title"/>
      </else-if>
      <else>
        <text variable="title" font-style="italic"/>
      </else>
    </choose>
    <choose>
      <if variable="URL">
        <text term="online" prefix=" [" suffix="]"/>
      </if>
    </choose>
  </macro>
  <macro name="number">
    <text variable="number"/>
  </macro>
  <macro name="medium">
    <text variable="medium"/>
  </macro>
  <macro name="genre">
    <choose>
      <if type="map">
        <choose>
          <if variable="genre">
            <text variable="genre" prefix="[" suffix="]"/>
          </if>
          <else>
            <text value="carte" prefix="[" suffix="]"/>
          </else>
        </choose>
      </if>
      <else>
        <text variable="genre"/>
      </else>
    </choose>
  </macro>
  <macro name="date">
    <choose>
      <if variable="issued">
        <date variable="issued">
          <date-part name="day" suffix=" de"/>
          <date-part name="month" suffix=" de"/>
          <date-part name="year"/>
        </date>
      </if>
    </choose>
  </macro>
  <macro name="edition">
    <text variable="edition" form="long"/>
  </macro>
  <macro name="publisher-place">
    <choose>
      <if type="patent manuscript article-newspaper broadcast motion_picture song entry-encyclopedia entry-dictionary" match="any">
        <choose>
          <if variable="publisher-place">
            <text variable="publisher-place"/>
          </if>
        </choose>
      </if>
      <else>
        <choose>
          <if variable="publisher-place">
            <text variable="publisher-place"/>
          </if>
          <else>
            <text value="s.l." text-case="capitalize-first"/>
          </else>
        </choose>
      </else>
    </choose>
  </macro>
  <macro name="issue">
    <group delimiter=", ">
      <text variable="volume" prefix="vol. "/>
      <text variable="issue" prefix="no. "/>
      <text variable="page" prefix="pp. "/>
    </group>
  </macro>
  <macro name="publisher">
    <choose>
      <if type="broadcast motion_picture song report entry-encyclopedia entry-dictionary" match="any">
        <choose>
          <if variable="publisher">
            <text variable="publisher"/>
          </if>
        </choose>
      </if>
      <else>
        <choose>
          <if variable="publisher">
            <text variable="publisher"/>
          </if>
          <else>
            <text value="s.n."/>
          </else>
        </choose>
      </else>
    </choose>
  </macro>
  <macro name="accessed">
    <choose>
      <if variable="URL">
        <group prefix=" [" suffix="]">
          <text term="accessed" text-case="capitalize-first"/>
          <date variable="accessed">
            <date-part name="day" prefix=" "/>
            <date-part name="month" prefix=" "/>
            <date-part name="year" prefix=" "/>
          </date>
        </group>
      </if>
    </choose>
  </macro>
  <macro name="collection">
    <group delimiter=", ">
      <text variable="collection-title"/>
      <choose>
        <if variable="collection-number">
          <text variable="collection-number"/>
        </if>
        <else>
          <text variable="number"/>
        </else>
      </choose>
    </group>
  </macro>
  <macro name="page">
    <choose>
      <if type="book thesis manuscript" match="any">
        <text variable="number-of-pages" suffix=" p"/>
      </if>
      <else-if type="chapter paper-conference article-newspaper" match="any">
        <text variable="page" prefix="pp. "/>
      </else-if>
      <else-if type="report patent" match="any">
        <text variable="page" suffix=" p"/>
      </else-if>
    </choose>
  </macro>
  <macro name="isbn">
    <text variable="ISBN" prefix="ISBN "/>
  </macro>
  <macro name="issn">
    <text variable="ISSN" prefix="ISSN "/>
  </macro>
  <macro name="doi">
    <text variable="DOI" prefix="DOI "/>
  </macro>
  <macro name="url">
    <choose>
      <if variable="URL">
        <group>
          <text term="retrieved" suffix=" " text-case="capitalize-first"/>
          <text term="from" suffix=": "/>
          <text variable="URL"/>
        </group>
      </if>
    </choose>
  </macro>
  <macro name="archive">
    <text variable="archive"/>
    <choose>
      <if variable="archive_location">
        <text value=": "/>
      </if>
    </choose>
  </macro>
  <macro name="archive_location">
    <choose>
      <if variable="archive_location">
        <text variable="archive_location"/>
      </if>
      <else>
        <text variable="call-number"/>
      </else>
    </choose>
  </macro>
  <citation et-al-min="4" et-al-use-first="1" disambiguate-add-year-suffix="true" disambiguate-add-names="true" disambiguate-add-givenname="true" collapse="year" year-suffix-delimiter=", " after-collapse-delimiter="; ">
    <layout prefix="(" suffix=")" delimiter="; ">
      <group delimiter=", p. ">
        <group delimiter=" ">
          <text macro="author-citation"/>
          <text macro="year-date"/>
        </group>
        <text variable="locator"/>
      </group>
    </layout>
  </citation>
  <bibliography hanging-indent="true">
    <sort>
      <key macro="author"/>
      <key macro="year-date"/>
      <key macro="title"/>
    </sort>
    <layout>
      <choose>
        <if type="book map" match="any">
          <group>
            <text macro="author" suffix=", "/>
            <text macro="year-date" suffix=". "/>
            <text macro="title" suffix=". "/>
            <text macro="genre" suffix=". "/>
            <text macro="edition" suffix=". "/>
            <text macro="publisher-place" suffix=": "/>
            <text macro="publisher" suffix=". "/>
            <text macro="accessed" suffix=". "/>
            <text macro="collection" suffix=". "/>
            <text macro="isbn" suffix=". "/>
            <text macro="url" suffix=". "/>
          </group>
        </if>
        <else-if type="article-journal article-magazine" match="any">
          <group>
            <text macro="author" suffix=", "/>
            <text macro="year-date" suffix=". "/>
            <text macro="title" suffix=", "/>
            <text macro="edition" suffix=". "/>
            <text macro="issue" suffix=". "/>
            <text macro="accessed" suffix=". "/>
            <text macro="issn" suffix=". "/>
            <text macro="doi" suffix=". "/>
            <text macro="url" suffix=". "/>
          </group>
        </else-if>
        <else-if type="article-newspaper">
          <group>
            <text macro="author" suffix=", "/>
            <text macro="year-date" suffix=". "/>
            <text macro="title" suffix=". "/>
            <text macro="edition" suffix=". "/>
            <text macro="publisher-place" suffix=", "/>
            <text macro="date" suffix=". "/>
            <text macro="page" suffix=". "/>
            <text macro="accessed" suffix=". "/>
            <text macro="issn" suffix=". "/>
            <text macro="url" suffix=". "/>
          </group>
        </else-if>
        <else-if type="entry entry-dictionary entry-encyclopedia" match="any">
          <group>
            <text macro="author" suffix=", "/>
            <text macro="year-date" suffix=". "/>
            <text macro="title" suffix=". "/>
            <text macro="edition" suffix=". "/>
            <text macro="publisher-place" suffix=": "/>
            <text macro="publisher" suffix=". "/>
            <text macro="collection" suffix=", "/>
            <text macro="page" suffix=". "/>
            <text macro="accessed" suffix=". "/>
            <text macro="isbn" suffix=". "/>
            <text macro="url" suffix=". "/>
          </group>
        </else-if>
        <else-if type="chapter">
          <group>
            <text macro="author" suffix=", "/>
            <text macro="year-date" suffix=". "/>
            <text macro="title" suffix=". "/>
            <text macro="edition" suffix=". "/>
            <text macro="publisher-place" suffix=": "/>
            <text macro="publisher" suffix=", "/>
            <text macro="collection" suffix=", "/>
            <text macro="page" suffix=". "/>
            <text macro="accessed" suffix=". "/>
            <text macro="isbn" suffix=". "/>
            <text macro="url" suffix=". "/>
          </group>
        </else-if>
        <else-if type="speech">
          <group>
            <text macro="author" suffix=", "/>
            <text macro="year-date" suffix=". "/>
            <text macro="title" suffix=". "/>
            <text macro="genre" suffix=". "/>
            <text macro="publisher-place" suffix=". "/>
            <text macro="accessed" suffix=". "/>
            <text macro="page" suffix=". "/>
            <text macro="url" suffix=". "/>
          </group>
        </else-if>
        <else-if type="paper-conference">
          <group>
            <text macro="author" suffix=", "/>
            <text macro="year-date" suffix=". "/>
            <text macro="title" suffix=". "/>
            <text macro="genre" suffix=". "/>
            <text macro="publisher-place" suffix=": "/>
            <text macro="publisher" suffix=", "/>
            <text macro="page" suffix=". "/>
            <text macro="accessed" suffix=". "/>
            <text macro="isbn" suffix=". "/>
            <text macro="doi" suffix=". "/>
            <text macro="url" suffix=". "/>
          </group>
        </else-if>
        <else-if type="thesis">
          <group>
            <text macro="author" suffix=", "/>
            <text macro="year-date" suffix=". "/>
            <text macro="title" suffix=". "/>
            <text macro="genre" suffix=". "/>
            <text macro="publisher-place" suffix=": "/>
            <text macro="publisher" suffix=". "/>
            <text macro="accessed" suffix=". "/>
            <text macro="url" suffix=". "/>
          </group>
        </else-if>
        <else-if type="post-weblog post webpage" match="any">
          <group>
            <text macro="author" suffix=", "/>
            <text macro="year-date" suffix=". "/>
            <text macro="title" suffix=". "/>
            <text macro="accessed" suffix=". "/>
            <text macro="url" suffix=". "/>
          </group>
        </else-if>
        <else-if type="broadcast motion_picture song" match="any">
          <group>
            <text macro="author" suffix=", "/>
            <text macro="year-date" suffix=". "/>
            <text macro="title" suffix=". "/>
            <text macro="medium" suffix=". "/>
            <text macro="publisher-place" suffix=": "/>
            <text macro="publisher" suffix=". "/>
            <text macro="accessed" suffix=". "/>
            <text macro="collection" suffix=". "/>
            <text macro="isbn" suffix=". "/>
            <text macro="url" suffix=". "/>
          </group>
        </else-if>
        <else-if type="report">
          <group>
            <text macro="author" suffix=", "/>
            <text macro="year-date" suffix=". "/>
            <text macro="title" suffix=". "/>
            <text macro="genre" suffix=". "/>
            <text macro="edition" suffix=". "/>
            <text macro="publisher-place" suffix=": "/>
            <text macro="publisher" suffix=". "/>
            <text macro="accessed" suffix=". "/>
            <text macro="collection" suffix=". "/>
            <text macro="url" suffix=". "/>
          </group>
        </else-if>
        <else-if type="manuscript">
          <group>
            <text macro="author" suffix=", "/>
            <text macro="year-date" suffix=". "/>
            <text macro="title" suffix=". "/>
            <text macro="genre" suffix=". "/>
            <text macro="edition" suffix=". "/>
            <text macro="publisher-place" suffix=". "/>
            <text macro="accessed" suffix=". "/>
            <text macro="collection" suffix=". "/>
            <text macro="url" suffix=". "/>
          </group>
        </else-if>
        <else-if type="patent">
          <group>
            <text macro="author" suffix=", "/>
            <text macro="year-date" suffix=". "/>
            <text macro="title" suffix=". "/>
            <text macro="number" suffix=". "/>
            <text macro="publisher-place" suffix=". "/>
            <text macro="accessed" suffix=". "/>
            <text macro="collection" suffix=". "/>
            <text macro="url" suffix=". "/>
          </group>
        </else-if>
        <else>
          <group>
            <text macro="author" suffix=", "/>
            <text macro="year-date" suffix=". "/>
            <text macro="title" suffix=". "/>
            <text macro="medium" suffix=". "/>
            <text macro="genre" suffix=". "/>
            <text macro="date" suffix=". "/>
            <text macro="edition" suffix=". "/>
            <text macro="publisher-place" suffix=": "/>
            <text macro="publisher" suffix=". "/>
            <text macro="accessed" suffix=". "/>
            <text macro="collection" suffix=". "/>
            <text macro="page" suffix=". "/>
            <text macro="isbn" suffix=". "/>
            <text macro="url" suffix=". "/>
          </group>
        </else>
      </choose>
      <group>
        <group display="block">
          <text macro="archive"/>
          <text macro="archive_location"/>
        </group>
      </group>
    </layout>
  </bibliography>
</style>
