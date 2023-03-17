<?xml version="1.0" encoding="utf-8"?>
<style xmlns="http://purl.org/net/xbiblio/csl" class="in-text" version="1.0" et-al-min="4">
  <info>
    <title>Guía PUCP</title>
    <id>http://www.zotero.org/styles/guia-pucp</id>
    <link rel="self" href="http://www.zotero.org/styles/guia-pucp"/>
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
    <contributor>
      <name>Brenton M. Wiernik</name>
      <email>zotero@wiernik.org</email>
    </contributor>
    <category citation-format="author-date"/>
    <category citation-format="author-date"/>
    <category field="generic-base"/>
    <updated>2023-03-17T16:51:46+00:00</updated>
    <updated>2023-03-16T15:51:53+00:00</updated>
    <rights license="http://creativecommons.org/licenses/by-sa/3.0/">This work is licensed under a Creative Commons Attribution-ShareAlike 3.0 License</rights>
    <link href="https://s3.amazonaws.com/files.pucp.edu.pe/homepucp/uploads/2016/06/08105745/Guia_PUCP_para_el_registro_y_citado_de_fuentes-2015.pdf"/>
  </info>
  <locale xml:lang="en">
    <terms>
      <term name="editortranslator" form="long">
        <single>editor &amp; traductor.</single>
        <multiple>editores. &amp; traductores.</multiple>
      </term>
      <term name="translator">traductor</term>
      <term name="interviewer" form="long">
        <single>entrevistador</single>
        <multiple>entrevistadores</multiple>
      </term>
      <term name="collection-editor" form="long">
        <single>editor</single>
        <multiple>editores</multiple>
      </term>
      <term name="bc">A.C.</term>
      <term name="ad">D.C.</term>
      <term name="letter">comunicación personal</term>
      <term name="letter" form="short">carta</term>
      <term name="issue" form="long">
        <term name="no author">AUTOR DESCONOCIDO.</term>
        <term name="no date">s/f</term>
        <term name="in">En</term>
        <term name="accessed">Consulta:</term>
        <term name="viewed">Vista:</term>
        <term name="month-01">enero</term>
        <term name="month-02">febrero</term>
        <term name="month-03">marzo</term>
        <term name="month-04">abril</term>
        <term name="month-05">mayo</term>
        <term name="month-06">junio</term>
        <term name="month-07">julio</term>
        <term name="month-08">agosto</term>
        <term name="month-09">septiembre</term>
        <term name="month-10">octubre</term>
        <term name="month-11">noviembre</term>
        <term name="month-12">diciembre</term>
        <term name="and">y</term>
        <term name="et-al">y otros</term>
        <single>número</single>
        <multiple>números</multiple>
      </term>
    </terms>
  </locale>
  <macro name="author-bib">
    <names variable="composer" delimiter=", ">
      <name and="text" delimiter-precedes-et-al="never" delimiter-precedes-last="never" et-al-min="4" et-al-use-first="1" initialize="false" name-as-sort-order="first"/>
      <name-part name="family" text-case="uppercase"/>
      <name-part name="given"/>
      <substitute>
        <names variable="author"/>
        <name-part name="family" text-case="uppercase"/>
        <name-part name="given"/>
        <names variable="illustrator"/>
        <name-part name="family" text-case="uppercase"/>
        <name-part name="given"/>
        <names variable="director">
          <name and="text" delimiter-precedes-last="always" et-al-min="4" et-al-use-first="1" initialize="false" name-as-sort-order="first"/>
          <name-part name="family" text-case="uppercase"/>
          <name-part name="given"/>
          <label form="long" prefix=" (" suffix=")" text-case="title"/>
        </names>
        <choose>
          <if variable="container-title">
            <choose>
              <if type="book entry entry-dictionary entry-encyclopedia" match="any">
                <choose>
                  <if variable="title">
                    <group delimiter=" ">
                      <text macro="title"/>
                      <text macro="parenthetical"/>
                    </group>
                  </if>
                  <else>
                    <text macro="title-and-descriptions"/>
                  </else>
                </choose>
              </if>
            </choose>
          </if>
        </choose>
        <names variable="editor" delimiter=", ">
          <name and="text" delimiter-precedes-et-al="never" delimiter-precedes-last="never" et-al-min="4" et-al-use-first="1" initialize="false" name-as-sort-order="first"/>
          <name-part name="family" text-case="uppercase"/>
          <name-part name="given"/>
          <label plural="always" text-case="title" prefix=" (" suffix=")"/>
        </names>
        <names variable="editorial-director">
          <name and="text" delimiter-precedes-et-al="never" delimiter-precedes-last="never" et-al-min="4" et-al-use-first="1" initialize="false" name-as-sort-order="all"/>
          <name-part name="family" text-case="uppercase"/>
          <name-part name="given"/>
          <label form="short" prefix=" (" suffix=")" text-case="title"/>
        </names>
        <names variable="collection-editor">
          <name and="text" delimiter-precedes-et-al="never" delimiter-precedes-last="never" et-al-min="4" et-al-use-first="1" initialize="false" name-as-sort-order="all"/>
          <name-part name="family" text-case="uppercase"/>
          <name-part name="given"/>
          <label form="short" prefix=" (" suffix=")" text-case="title"/>
        </names>
        <choose>
          <if variable="title">
            <group delimiter=" ">
              <text macro="title"/>
              <text macro="parenthetical"/>
            </group>
          </if>
          <else>
            <text macro="title-and-descriptions"/>
          </else>
        </choose>
      </substitute>
    </names>
  </macro>
  <macro name="author-intext">
    <choose>
      <else>
        <names variable="composer" delimiter=",">
          <name form="short" and="text" delimiter-precedes-et-al="never" delimiter-precedes-last="never" et-al-min="4" et-al-use-first="1" initialize="false"/>
          <substitute>
            <names variable="author"/>
            <names variable="illustrator"/>
            <names variable="director"/>
            <choose>
              <if variable="container-title">
                <choose>
                  <if type="book entry entry-dictionary entry-encyclopedia" match="any">
                    <text macro="title-intext"/>
                  </if>
                </choose>
              </if>
            </choose>
            <names variable="editor"/>
            <names variable="editorial-director"/>
            <text macro="title-intext"/>
          </substitute>
        </names>
      </else>
    </choose>
  </macro>
  <macro name="date-bib">
    <group delimiter="" suffix="">
      <choose>
        <if is-uncertain-date="issued">
          <text term="circa" form="short"/>
        </if>
      </choose>
      <group>
        <choose>
          <if variable="issued">
            <date variable="issued">
              <date-part name="year"/>
            </date>
            <text variable="year-suffix"/>
            <choose>
              <if type="article-magazine article-newspaper broadcast interview motion_picture pamphlet personal_communication post post-weblog song speech webpage" match="any">
                <date variable="issued">
                  <date-part prefix=", " name="month"/>
                  <date-part prefix=" " name="day"/>
                </date>
              </if>
              <else-if type="paper-conference">
                <choose>
                  <if variable="collection-editor editor editorial-director issue page volume" match="none">
                    <date variable="issued">
                      <date-part prefix=", " name="month"/>
                      <date-part prefix=" " name="day"/>
                    </date>
                  </if>
                </choose>
              </else-if>
            </choose>
          </if>
          <else-if variable="status">
            <group>
              <text variable="status" text-case="lowercase"/>
              <text variable="year-suffix" prefix="-"/>
            </group>
          </else-if>
          <else>
            <text term="no date" form="short"/>
            <text variable="year-suffix" prefix="-"/>
          </else>
        </choose>
      </group>
    </group>
  </macro>
  <macro name="date-sort-group">
    <choose>
      <if variable="issued">
        <text value="1"/>
      </if>
      <else-if variable="status">
        <text value="2"/>
      </else-if>
      <else>
        <text value="0"/>
      </else>
    </choose>
  </macro>
  <macro name="date-sort-date">
    <choose>
      <if type="article-magazine article-newspaper broadcast interview pamphlet personal_communication post post-weblog speech treaty webpage" match="any">
        <date variable="issued" form="numeric"/>
      </if>
      <else-if type="paper-conference">
        <choose>
          <if variable="collection-editor editor editorial-director issue page volume" match="none">
            <date variable="issued" form="numeric"/>
          </if>
        </choose>
      </else-if>
      <else>
        <date variable="issued" form="numeric"/>
      </else>
    </choose>
  </macro>
  <macro name="date-intext">
    <choose>
      <if variable="issued">
        <group delimiter="/">
          <group delimiter=" ">
            <choose>
              <if is-uncertain-date="original-date">
                <text term="circa" form="short"/>
              </if>
            </choose>
            <date variable="original-date">
              <date-part name="year"/>
            </date>
          </group>
          <group delimiter=" ">
            <choose>
              <if is-uncertain-date="issued">
                <text term="circa" form="short"/>
              </if>
            </choose>
            <group>
              <choose>
                <if type="interview personal_communication" match="any">
                  <choose>
                    <if variable="archive container-title DOI publisher URL" match="none">
                      <date variable="issued" form="text"/>
                    </if>
                    <else>
                      <date variable="issued">
                        <date-part name="year"/>
                      </date>
                    </else>
                  </choose>
                </if>
                <else>
                  <date variable="issued">
                    <date-part name="year"/>
                  </date>
                </else>
              </choose>
              <text variable="year-suffix"/>
            </group>
          </group>
        </group>
      </if>
      <else-if variable="status">
        <text variable="status" text-case="lowercase"/>
        <text variable="year-suffix" prefix="-"/>
      </else-if>
      <else>
        <text term="no date" form="short"/>
        <text variable="year-suffix" prefix="-"/>
      </else>
    </choose>
  </macro>
  <macro name="title-and-descriptions">
    <choose>
      <if variable="title">
        <group delimiter=" ">
          <text macro="title"/>
          <text macro="parenthetical"/>
          <text macro="bracketed"/>
        </group>
      </if>
      <else>
        <group delimiter=" ">
          <text macro="bracketed"/>
          <text macro="parenthetical"/>
        </group>
      </else>
    </choose>
  </macro>
  <macro name="title">
    <choose>
      <if type="post webpage" match="any">
        <text variable="title" font-style="italic" suffix=". "/>
      </if>
      <else-if variable="container-title" match="any">
        <text variable="title" strip-periods="false" quotes="true" suffix=". "/>
      </else-if>
      <else>
        <choose>
          <if type="article-journal article-magazine article-newspaper post-weblog review review-book" match="any">
            <text variable="title" font-style="italic" suffix=". "/>
          </if>
          <if type="report" match="any">
            <text variable="title" font-style="italic"/>
          </if>
          <else-if type="paper-conference">
            <choose>
              <if variable="collection-editor editor editorial-director" match="any">
                <group delimiter=": " font-style="italic">
                  <text variable="title" suffix=". "/>
                  <choose>
                    <if is-numeric="volume" match="none">
                      <group delimiter=" ">
                        <label variable="volume" form="short" text-case="capitalize-first"/>
                        <text variable="volume"/>
                      </group>
                    </if>
                  </choose>
                </group>
              </if>
              <else>
                <text variable="title" font-style="italic" suffix=". "/>
              </else>
            </choose>
          </else-if>
          <else>
            <group delimiter=": " font-style="italic">
              <text variable="title" suffix=". "/>
              <choose>
                <if is-numeric="volume" match="none">
                  <group delimiter=" ">
                    <label variable="volume" form="short" text-case="capitalize-first"/>
                    <text variable="volume"/>
                  </group>
                </if>
              </choose>
            </group>
          </else>
        </choose>
      </else>
    </choose>
  </macro>
  <macro name="title-intext">
    <choose>
      <if variable="title" match="none">
        <text macro="bracketed-intext" prefix="[" suffix="]"/>
      </if>
      <else-if type="bill">
        <choose>
          <if variable="number container-title" match="none">
            <text variable="title" form="short" font-style="italic" text-case="title"/>
          </if>
          <else-if variable="title">
            <text variable="title" form="short" text-case="title"/>
          </else-if>
          <else>
            <group delimiter=" ">
              <text variable="genre"/>
              <group delimiter=" ">
                <choose>
                  <if variable="chapter-number container-title" match="none">
                    <text term="issue" form="short"/>
                  </if>
                </choose>
                <text variable="number"/>
              </group>
            </group>
          </else>
        </choose>
      </else-if>
      <else-if type="legal_case" match="any">
        <text variable="title" font-style="italic"/>
      </else-if>
      <else-if type="legislation treaty" match="any">
        <text variable="title" form="short" text-case="title"/>
      </else-if>
      <else-if type="post webpage" match="any">
        <text variable="title" form="short" font-style="italic" text-case="title"/>
      </else-if>
      <else-if variable="container-title" match="any">
        <text variable="title" form="short" quotes="true" text-case="title"/>
      </else-if>
      <else>
        <text variable="title" form="short" font-style="italic" text-case="title"/>
      </else>
    </choose>
  </macro>
  <macro name="parenthetical">
    <group>
      <choose>
        <if type="patent">
          <group delimiter=" ">
            <text variable="authority" form="short"/>
            <choose>
              <if variable="genre">
                <text variable="genre" text-case="capitalize-first"/>
              </if>
              <else>
                <text value="patent" text-case="capitalize-first"/>
              </else>
            </choose>
            <group delimiter=" ">
              <text term="issue" form="short" text-case="capitalize-first"/>
              <text variable="number"/>
            </group>
          </group>
        </if>
        <else-if type="post webpage" match="any">
          <group delimiter="; ">
            <text macro="secondary-contributors"/>
            <text macro="database-location"/>
            <text macro="number"/>
            <text macro="locators-booklike"/>
          </group>
        </else-if>
        <else-if variable="container-title">
          <group delimiter="; ">
            <text macro="secondary-contributors"/>
            <choose>
              <if type="broadcast graphic map motion_picture song" match="any">
                <text macro="number"/>
              </if>
            </choose>
          </group>
        </else-if>
        <else>
          <group delimiter="; ">
            <text macro="secondary-contributors"/>
            <text macro="database-location"/>
            <text macro="number"/>
            <text macro="locators-booklike"/>
          </group>
        </else>
      </choose>
    </group>
  </macro>
  <macro name="parenthetical-container">
    <choose>
      <if variable="container-title" match="any">
        <group prefix="(" suffix=")">
          <group delimiter="; ">
            <text macro="database-location"/>
            <choose>
              <if type="broadcast graphic map motion_picture song" match="none">
                <text macro="number"/>
              </if>
            </choose>
            <text macro="locators-booklike"/>
          </group>
        </group>
      </if>
    </choose>
  </macro>
  <macro name="bracketed">
    <group prefix="[" suffix="]">
      <choose>
        <if variable="reviewed-author reviewed-title" type="review review-book" match="any">
          <group delimiter="; ">
            <group delimiter=", ">
              <group delimiter=" ">
                <choose>
                  <if variable="number" match="none">
                    <choose>
                      <if variable="genre">
                        <text variable="genre" text-case="capitalize-first"/>
                      </if>
                      <else-if variable="medium">
                        <text variable="medium" text-case="capitalize-first"/>
                      </else-if>
                      <else>
                        <text value="Review of"/>
                      </else>
                    </choose>
                  </if>
                  <else>
                    <choose>
                      <if variable="medium">
                        <text variable="medium" text-case="capitalize-first"/>
                      </if>
                      <else>
                        <text value="Review of"/>
                      </else>
                    </choose>
                  </else>
                </choose>
                <text macro="reviewed-title"/>
              </group>
              <names variable="reviewed-author">
                <label form="verb-short" suffix=" "/>
                <name and="symbol" initialize-with=". " delimiter=", "/>
              </names>
            </group>
            <choose>
              <if variable="genre" match="any">
                <choose>
                  <if variable="number" match="none">
                    <text variable="medium" text-case="capitalize-first"/>
                  </if>
                </choose>
              </if>
            </choose>
          </group>
        </if>
        <else-if type="thesis">
          <group delimiter="; ">
            <choose>
              <if variable="number" match="none">
                <group delimiter=", ">
                  <text variable="genre" text-case="capitalize-first"/>
                  <choose>
                    <if variable="archive DOI URL" match="any">
                      <text variable="publisher"/>
                    </if>
                  </choose>
                </group>
              </if>
            </choose>
            <text variable="medium" text-case="capitalize-first"/>
          </group>
        </else-if>
        <else-if variable="interviewer" type="interview" match="any">
          <choose>
            <if variable="title">
              <text macro="format"/>
            </if>
            <else-if variable="genre">
              <group delimiter="; ">
                <group delimiter=" ">
                  <text variable="genre" text-case="capitalize-first"/>
                  <group delimiter=" ">
                    <text term="author" form="verb"/>
                    <names variable="interviewer">
                      <name and="symbol" initialize-with=". " delimiter=", "/>
                    </names>
                  </group>
                </group>
              </group>
            </else-if>
            <else-if variable="interviewer">
              <group delimiter="; ">
                <names variable="interviewer">
                  <label form="verb" suffix=" " text-case="capitalize-first"/>
                  <name and="symbol" initialize-with=". " delimiter=", "/>
                </names>
                <text variable="medium" text-case="capitalize-first"/>
              </group>
            </else-if>
            <else>
              <text macro="format"/>
            </else>
          </choose>
        </else-if>
        <else-if type="personal_communication">
          <choose>
            <if variable="recipient">
              <group delimiter="; ">
                <group delimiter=" ">
                  <choose>
                    <if variable="number" match="none">
                      <choose>
                        <if variable="genre">
                          <text variable="genre" text-case="capitalize-first"/>
                        </if>
                        <else-if variable="medium">
                          <text variable="medium" text-case="capitalize-first"/>
                        </else-if>
                        <else>
                          <text term="letter" form="short" text-case="capitalize-first"/>
                        </else>
                      </choose>
                    </if>
                    <else>
                      <choose>
                        <if variable="medium">
                          <text variable="medium" text-case="capitalize-first"/>
                        </if>
                        <else>
                          <text term="letter" form="short" text-case="capitalize-first"/>
                        </else>
                      </choose>
                    </else>
                  </choose>
                  <names variable="recipient" delimiter=", ">
                    <label form="verb" suffix=" "/>
                    <name and="symbol" delimiter=", "/>
                  </names>
                </group>
                <choose>
                  <if variable="genre" match="any">
                    <choose>
                      <if variable="number" match="none">
                        <text variable="medium" text-case="capitalize-first"/>
                      </if>
                    </choose>
                  </if>
                </choose>
              </group>
            </if>
            <else>
              <text macro="format"/>
            </else>
          </choose>
        </else-if>
        <else-if variable="composer" type="song" match="all">
          <group delimiter="; ">
            <choose>
              <if variable="number" match="none">
                <group delimiter=" ">
                  <choose>
                    <if variable="genre">
                      <text variable="genre" text-case="capitalize-first"/>
                      <names variable="author" prefix="recorded by ">
                        <name and="symbol" initialize-with=". " delimiter=", "/>
                      </names>
                    </if>
                    <else-if variable="medium">
                      <text variable="medium" text-case="capitalize-first"/>
                      <names variable="author" prefix="recorded by ">
                        <name and="symbol" initialize-with=". " delimiter=", "/>
                      </names>
                    </else-if>
                    <else>
                      <names variable="author" prefix="Recorded by ">
                        <name and="symbol" initialize-with=". " delimiter=", "/>
                      </names>
                    </else>
                  </choose>
                </group>
              </if>
              <else>
                <group delimiter=" ">
                  <choose>
                    <if variable="medium">
                      <text variable="medium" text-case="capitalize-first"/>
                      <names variable="author" prefix="recorded by ">
                        <name and="symbol" initialize-with=". " delimiter=", "/>
                      </names>
                    </if>
                    <else>
                      <names variable="author" prefix="Recorded by ">
                        <name and="symbol" initialize-with=". " delimiter=", "/>
                      </names>
                    </else>
                  </choose>
                </group>
              </else>
            </choose>
            <choose>
              <if variable="genre" match="any">
                <choose>
                  <if variable="number" match="none">
                    <text variable="medium" text-case="capitalize-first"/>
                  </if>
                </choose>
              </if>
            </choose>
          </group>
        </else-if>
        <else-if variable="container-title" match="none">
          <text macro="format"/>
        </else-if>
        <else>
          <choose>
            <if type="paper-conference speech" match="any">
              <choose>
                <if variable="collection-editor editor editorial-director issue page volume" match="any">
                  <text macro="format"/>
                </if>
              </choose>
            </if>
            <else-if type="book">
              <choose>
                <if variable="version" match="none">
                  <text macro="format"/>
                </if>
              </choose>
            </else-if>
            <else-if type="report" match="none">
              <text macro="format"/>
            </else-if>
          </choose>
        </else>
      </choose>
    </group>
  </macro>
  <macro name="bracketed-intext">
    <group prefix="[" suffix="]">
      <choose>
        <if variable="reviewed-author reviewed-title" type="review review-book" match="any">
          <text macro="reviewed-title-intext" prefix="Review of "/>
        </if>
        <else-if variable="interviewer" type="interview" match="any">
          <names variable="interviewer">
            <label form="verb" suffix=" " text-case="capitalize-first"/>
            <name and="symbol" initialize-with=". " delimiter=", "/>
            <substitute>
              <text macro="format-intext"/>
            </substitute>
          </names>
        </else-if>
        <else-if type="personal_communication">
          <choose>
            <if variable="recipient">
              <group delimiter=" ">
                <choose>
                  <if variable="number" match="none">
                    <text variable="genre" text-case="capitalize-first"/>
                  </if>
                  <else>
                    <text term="letter" form="short" text-case="capitalize-first"/>
                  </else>
                </choose>
                <names variable="recipient" delimiter=", ">
                  <label form="verb" suffix=" "/>
                  <name and="symbol" delimiter=", "/>
                </names>
              </group>
            </if>
            <else>
              <text macro="format-intext"/>
            </else>
          </choose>
        </else-if>
        <else>
          <text macro="format-intext"/>
        </else>
      </choose>
    </group>
  </macro>
  <macro name="bracketed-container">
    <group prefix="[" suffix="]">
      <choose>
        <if type="paper-conference speech" match="any">
          <choose>
            <if variable="collection-editor editor editorial-director issue page volume" match="none">
              <text macro="format"/>
            </if>
          </choose>
        </if>
        <else-if type="book" variable="version" match="all">
          <text macro="format"/>
        </else-if>
        <else-if type="report">
          <text macro="format"/>
        </else-if>
      </choose>
    </group>
  </macro>
  <macro name="secondary-contributors">
    <choose>
      <if type="article-journal article-magazine article-newspaper post-weblog review review-book" match="any">
        <text macro="secondary-contributors-periodical"/>
      </if>
      <else-if type="paper-conference">
        <choose>
          <if variable="collection-editor editor editorial-director" match="any">
            <text macro="secondary-contributors-booklike"/>
          </if>
          <else>
            <text macro="secondary-contributors-periodical"/>
          </else>
        </choose>
      </else-if>
      <else>
        <text macro="secondary-contributors-booklike"/>
      </else>
    </choose>
  </macro>
  <macro name="secondary-contributors-periodical">
    <group delimiter="; ">
      <choose>
        <if variable="title">
          <names variable="interviewer" delimiter="; ">
            <name and="symbol" initialize-with=". " delimiter=", "/>
            <label form="short" prefix=", " text-case="title"/>
          </names>
        </if>
      </choose>
      <names variable="translator" delimiter="; ">
        <name and="symbol" initialize-with=". " delimiter=", "/>
        <label form="short" prefix=", " text-case="title"/>
      </names>
    </group>
  </macro>
  <macro name="secondary-contributors-booklike">
    <group delimiter="; ">
      <choose>
        <if variable="title">
          <names variable="interviewer">
            <name and="symbol" initialize-with=". " delimiter=", "/>
            <label form="short" prefix=", " text-case="title"/>
          </names>
        </if>
      </choose>
    </group>
  </macro>
  <macro name="database-location">
    <choose>
      <if variable="archive-place" match="none">
        <text variable="archive_location"/>
      </if>
    </choose>
  </macro>
  <macro name="number">
    <choose>
      <if variable="number">
        <group delimiter=", ">
          <group delimiter=" ">
            <text variable="genre" text-case="title" prefix="[" suffix="]"/>
          </group>
          <choose>
            <if type="thesis">
              <choose>
                <if variable="archive DOI URL" match="any">
                  <text variable="publisher"/>
                </if>
              </choose>
            </if>
          </choose>
        </group>
      </if>
    </choose>
  </macro>
  <macro name="locators-booklike">
    <choose>
      <if type="article-journal article-magazine article-newspaper broadcast interview patent post post-weblog review review-book speech webpage" match="any"/>
      <else-if type="paper-conference">
        <choose>
          <if variable="collection-editor editor editorial-director" match="any">
            <group delimiter=", ">
              <text macro="version"/>
              <text macro="edition"/>
              <text macro="volume-booklike"/>
            </group>
          </if>
        </choose>
      </else-if>
      <else>
        <group delimiter=", ">
          <text macro="version"/>
          <text macro="edition"/>
          <text macro="volume-booklike"/>
        </group>
      </else>
    </choose>
  </macro>
  <macro name="version">
    <choose>
      <if is-numeric="version">
        <group delimiter=" ">
          <text term="version" text-case="capitalize-first"/>
          <text variable="version"/>
        </group>
      </if>
      <else>
        <text variable="version"/>
      </else>
    </choose>
  </macro>
  <macro name="edition">
    <choose>
      <if is-numeric="edition">
        <group delimiter=" ">
          <number text-case="lowercase" variable="edition" form="ordinal"/>
          <label variable="edition"/>
        </group>
      </if>
      <else>
        <text variable="edition"/>
      </else>
    </choose>
  </macro>
  <macro name="volume-booklike">
    <group delimiter=", ">
      <choose>
        <if type="report">
          <group delimiter=" ">
            <text variable="collection-title" text-case="title"/>
            <text variable="collection-number"/>
          </group>
        </if>
      </choose>
      <choose>
        <if variable="volume" match="any">
          <choose>
            <if is-numeric="volume" match="none"/>
            <else>
              <group delimiter=" ">
                <label variable="volume" form="short" text-case="capitalize-first"/>
                <number variable="volume" form="numeric"/>
              </group>
            </else>
          </choose>
        </if>
        <else>
          <group>
            <text term="volume" form="short" text-case="capitalize-first" suffix=" "/>
            <text term="page-range-delimiter" prefix="1"/>
            <number variable="number-of-volumes" form="numeric"/>
          </group>
        </else>
      </choose>
      <group delimiter=" ">
        <label variable="issue" text-case="capitalize-first"/>
        <text variable="issue"/>
      </group>
      <group delimiter=" ">
        <label variable="page" form="short" suffix=" "/>
        <text variable="page"/>
      </group>
    </group>
  </macro>
  <macro name="reviewed-title">
    <choose>
      <if variable="reviewed-title">
        <text variable="reviewed-title" font-style="italic"/>
      </if>
      <else>
        <text variable="title" font-style="italic"/>
      </else>
    </choose>
  </macro>
  <macro name="reviewed-title-intext">
    <choose>
      <if variable="reviewed-title">
        <text variable="reviewed-title" form="short" font-style="italic" text-case="title"/>
      </if>
      <else>
        <text variable="title" form="short" font-style="italic" text-case="title"/>
      </else>
    </choose>
  </macro>
  <macro name="format">
    <choose>
      <if variable="genre medium" match="any">
        <group delimiter="; ">
          <choose>
            <if variable="number" match="none">
              <text variable="genre" text-case="capitalize-first"/>
            </if>
          </choose>
          <text variable="medium" text-case="capitalize-first"/>
        </group>
      </if>
      <else-if type="dataset">
        <text value="Data set"/>
      </else-if>
      <else-if type="book" variable="version" match="all">
        <text value="Computer software"/>
      </else-if>
      <else-if type="interview personal_communication" match="any">
        <choose>
          <if variable="archive container-title DOI publisher URL" match="none">
            <text term="letter" text-case="capitalize-first"/>
          </if>
          <else-if type="interview">
            <text term="interview" text-case="capitalize-first"/>
          </else-if>
        </choose>
      </else-if>
      <else-if type="map">
        <text value="Map"/>
      </else-if>
    </choose>
  </macro>
  <macro name="format-intext">
    <choose>
      <if variable="genre" match="any">
        <text variable="genre" text-case="capitalize-first"/>
      </if>
      <else-if variable="medium">
        <text variable="medium" text-case="capitalize-first"/>
      </else-if>
      <else-if type="dataset">
        <text value="Data set"/>
      </else-if>
      <else-if type="book" variable="version" match="all">
        <text value="Computer software"/>
      </else-if>
      <else-if type="interview personal_communication" match="any">
        <choose>
          <if variable="archive container-title DOI publisher URL" match="none">
            <text term="letter" text-case="capitalize-first"/>
          </if>
          <else-if type="interview">
            <text term="interview" text-case="capitalize-first"/>
          </else-if>
        </choose>
      </else-if>
      <else-if type="map">
        <text value="Map"/>
      </else-if>
    </choose>
  </macro>
  <macro name="container">
    <choose>
      <if type="article-journal article-magazine article-newspaper post-weblog review review-book" match="any">
        <text macro="container-periodical"/>
      </if>
      <else-if type="paper-conference">
        <choose>
          <if variable="editor editorial-director collection-editor container-author" match="any">
            <text macro="container-booklike"/>
          </if>
          <else>
            <text macro="container-periodical"/>
          </else>
        </choose>
      </else-if>
      <else-if type="post webpage" match="none">
        <text macro="container-booklike"/>
      </else-if>
    </choose>
  </macro>
  <macro name="container-periodical">
    <group delimiter=". ">
      <group delimiter=", ">
        <text variable="container-title" font-style="italic" text-case="title"/>
        <choose>
          <if variable="volume">
            <group delimiter=", ">
              <text variable="volume" font-style="normal" prefix="volumen "/>
              <text variable="issue" prefix="número "/>
            </group>
          </if>
          <else>
            <text variable="issue" font-style="italic"/>
          </else>
        </choose>
        <choose>
          <if variable="page">
            <text variable="page"/>
          </if>
          <else>
            <text variable="number" prefix="Article "/>
          </else>
        </choose>
      </group>
      <choose>
        <if variable="issued">
          <choose>
            <if variable="issue page volume" match="none">
              <text variable="status" text-case="capitalize-first"/>
            </if>
          </choose>
        </if>
      </choose>
    </group>
  </macro>
  <macro name="container-booklike">
    <choose>
      <if variable="container-title" match="any">
        <group delimiter=" ">
          <text term="in" text-case="capitalize-first"/>
          <group delimiter=", ">
            <names variable="editor translator">
              <name font-variant="normal" and="text" delimiter-precedes-et-al="never" delimiter-precedes-last="never" et-al-min="4" et-al-use-first="1" initialize="false" name-as-sort-order="first"/>
              <label text-case="title" prefix=" (" suffix=")"/>
              <substitute>
                <names variable="editorial-director"/>
                <names variable="collection-editor"/>
                <names variable="container-author"/>
              </substitute>
            </names>
            <group delimiter=": " font-style="italic">
              <text variable="container-title" suffix=". "/>
              <choose>
                <if is-numeric="volume" match="none">
                  <group delimiter=" ">
                    <label variable="volume" form="short" text-case="capitalize-first"/>
                    <text variable="volume"/>
                  </group>
                </if>
              </choose>
            </group>
          </group>
          <text macro="parenthetical-container"/>
          <text macro="bracketed-container"/>
        </group>
      </if>
    </choose>
  </macro>
  <macro name="publisher">
    <group delimiter="; ">
      <choose>
        <if type="thesis">
          <choose>
            <if variable="archive DOI URL" match="none">
              <text variable="publisher"/>
            </if>
          </choose>
        </if>
        <else-if type="post webpage" match="any">
          <group delimiter="; ">
            <text variable="container-title" text-case="title"/>
            <text variable="publisher"/>
          </group>
        </else-if>
        <else-if type="paper-conference">
          <choose>
            <if variable="collection-editor editor editorial-director" match="any">
              <text variable="publisher"/>
            </if>
          </choose>
        </else-if>
        <else-if type="article-journal article-magazine article-newspaper post-weblog" match="none">
          <text variable="publisher"/>
        </else-if>
      </choose>
      <group delimiter=", ">
        <choose>
          <if variable="archive-place">
            <text variable="archive_location"/>
          </if>
        </choose>
        <text variable="archive"/>
        <text variable="archive-place"/>
      </group>
    </group>
  </macro>
  <macro name="access">
    <choose>
      <if variable="DOI" match="any">
        <text variable="DOI" prefix="https://doi.org/"/>
      </if>
      <else-if variable="URL">
        <group delimiter=" ">
          <choose>
            <if variable="issued status" match="none">
              <group delimiter=" ">
                <text term="retrieved" text-case="capitalize-first"/>
                <date variable="accessed" form="text" suffix=","/>
                <text term="from"/>
              </group>
            </if>
          </choose>
          <text variable="URL"/>
        </group>
      </else-if>
    </choose>
  </macro>
  <macro name="event">
    <choose>
      <if variable="event">
        <choose>
          <if variable="collection-editor editor editorial-director issue page volume" match="none">
            <group delimiter=", ">
              <text variable="event"/>
              <text variable="event-place"/>
            </group>
          </if>
        </choose>
      </if>
    </choose>
  </macro>
  <macro name="publication-history">
    <choose>
      <if type="patent" match="none">
        <group prefix="(" suffix=")">
          <choose>
            <if variable="references">
              <text variable="references"/>
            </if>
            <else>
              <group delimiter=" ">
                <text value="Original work published"/>
                <choose>
                  <if is-uncertain-date="original-date">
                    <text term="circa" form="short"/>
                  </if>
                </choose>
                <date variable="original-date">
                  <date-part name="year"/>
                </date>
              </group>
            </else>
          </choose>
        </group>
      </if>
      <else>
        <text variable="references" prefix="(" suffix=")"/>
      </else>
    </choose>
  </macro>
  <macro name="legal-cites">
    <choose>
      <if type="legal_case">
        <group delimiter=". ">
          <group delimiter=", ">
            <text variable="title"/>
            <group delimiter=" ">
              <text macro="container-legal"/>
              <text macro="date-legal"/>
            </group>
            <text variable="references"/>
          </group>
          <text macro="access"/>
        </group>
      </if>
      <else-if type="bill">
        <group delimiter=". ">
          <group delimiter=", ">
            <choose>
              <if variable="number container-title" match="none">
                <text variable="title" font-style="italic"/>
              </if>
              <else>
                <text variable="title"/>
              </else>
            </choose>
            <group delimiter=" ">
              <text macro="container-legal"/>
              <text macro="date-legal"/>
              <choose>
                <if variable="number container-title" match="none">
                  <names variable="author" prefix="(testimony of " suffix=")">
                    <name and="symbol" delimiter=", "/>
                  </names>
                </if>
                <else>
                  <text variable="status" prefix="(" suffix=")"/>
                </else>
              </choose>
            </group>
            <text variable="references"/>
          </group>
          <text macro="access"/>
        </group>
      </else-if>
      <else-if type="legislation">
        <group delimiter=". ">
          <group delimiter=", ">
            <text variable="title"/>
            <group delimiter=" ">
              <text macro="container-legal"/>
              <text macro="date-legal"/>
              <text variable="status" prefix="(" suffix=")"/>
            </group>
            <text variable="references"/>
          </group>
          <text macro="access"/>
        </group>
      </else-if>
      <else-if type="treaty">
        <group delimiter=", ">
          <text variable="title" text-case="title"/>
          <names variable="author">
            <name initialize-with="." form="short" delimiter="-"/>
          </names>
          <text macro="date-legal"/>
          <text macro="container-legal"/>
          <text macro="access"/>
        </group>
      </else-if>
    </choose>
  </macro>
  <macro name="date-legal">
    <choose>
      <if type="legal_case">
        <group prefix="(" suffix=")" delimiter=" ">
          <text variable="authority"/>
          <choose>
            <if variable="container-title" match="any">
              <date variable="issued" form="numeric" date-parts="year"/>
            </if>
            <else>
              <date variable="issued" form="text"/>
            </else>
          </choose>
        </group>
      </if>
      <else-if type="bill legislation" match="any">
        <group prefix="(" suffix=")" delimiter=" ">
          <group delimiter=" ">
            <date variable="original-date">
              <date-part name="year"/>
            </date>
            <text term="and" form="symbol"/>
          </group>
          <date variable="issued">
            <date-part name="year"/>
          </date>
        </group>
      </else-if>
      <else-if type="treaty">
        <date variable="issued" form="text"/>
      </else-if>
    </choose>
  </macro>
  <macro name="container-legal">
    <choose>
      <if type="legal_case">
        <group delimiter=" ">
          <choose>
            <if variable="container-title">
              <group delimiter=" ">
                <text variable="volume"/>
                <text variable="container-title"/>
                <group delimiter=" ">
                  <text term="section" form="symbol"/>
                  <text variable="section"/>
                </group>
                <choose>
                  <if variable="page page-first" match="any">
                    <text variable="page-first"/>
                  </if>
                  <else>
                    <text value="___"/>
                  </else>
                </choose>
              </group>
            </if>
            <else>
              <group delimiter=" ">
                <choose>
                  <if is-numeric="number">
                    <text term="issue" form="short" text-case="capitalize-first"/>
                  </if>
                </choose>
                <text variable="number"/>
              </group>
            </else>
          </choose>
        </group>
      </if>
      <else-if type="bill">
        <group delimiter=", ">
          <group delimiter=" ">
            <text variable="genre"/>
            <group delimiter=" ">
              <choose>
                <if variable="chapter-number container-title" match="none">
                  <text term="issue" form="short"/>
                </if>
              </choose>
              <text variable="number"/>
            </group>
          </group>
          <text variable="authority"/>
          <text variable="chapter-number"/>
          <group delimiter=" ">
            <text variable="volume"/>
            <text variable="container-title"/>
            <text variable="page-first"/>
          </group>
        </group>
      </else-if>
      <else-if type="legislation">
        <choose>
          <if variable="number">
            <group delimiter=", ">
              <text variable="number" prefix="Pub. L. No. "/>
              <group delimiter=" ">
                <text variable="volume"/>
                <text variable="container-title"/>
                <text variable="page-first"/>
              </group>
            </group>
          </if>
          <else>
            <group delimiter=" ">
              <text variable="volume"/>
              <text variable="container-title"/>
              <choose>
                <if variable="section">
                  <group delimiter=" ">
                    <text term="section" form="symbol"/>
                    <text variable="section"/>
                  </group>
                </if>
                <else>
                  <text variable="page-first"/>
                </else>
              </choose>
            </group>
          </else>
        </choose>
      </else-if>
      <else-if type="treaty">
        <group delimiter=" ">
          <number variable="volume"/>
          <text variable="container-title"/>
          <choose>
            <if variable="page page-first" match="any">
              <text variable="page-first"/>
            </if>
            <else>
              <group delimiter=" ">
                <text term="issue" form="short" text-case="capitalize-first"/>
                <text variable="number"/>
              </group>
            </else>
          </choose>
        </group>
      </else-if>
    </choose>
  </macro>
  <macro name="citation-locator">
    <group delimiter=" ">
      <choose>
        <if locator="chapter">
          <label variable="locator" text-case="capitalize-first"/>
        </if>
        <else>
          <label variable="locator" form="short"/>
        </else>
      </choose>
      <text variable="locator"/>
    </group>
  </macro>
  <citation et-al-min="4" et-al-use-first="1" disambiguate-add-names="true" disambiguate-add-givenname="true" disambiguate-add-year-suffix="true" givenname-disambiguation-rule="primary-name-with-initials" collapse="year">
    <sort>
      <key macro="author-bib" names-min="3" names-use-first="1"/>
      <key macro="date-sort-group"/>
      <key macro="date-sort-date" sort="ascending"/>
      <key variable="status"/>
    </sort>
    <layout delimiter=", " prefix="(" suffix=")">
      <group delimiter=" ">
        <text macro="author-intext"/>
        <text macro="date-intext"/>
        <text macro="citation-locator" prefix=": "/>
      </group>
    </layout>
  </citation>
  <bibliography hanging-indent="true" et-al-min="21" et-al-use-first="19" et-al-use-last="true" entry-spacing="0" line-spacing="2">
    <sort>
      <key macro="author-bib"/>
      <key macro="date-sort-group"/>
      <key macro="date-sort-date" sort="ascending"/>
      <key variable="status"/>
      <key macro="title"/>
    </sort>
    <layout>
      <choose>
        <if type="bill legal_case legislation treaty" match="any">
          <choose>
            <if variable="DOI URL" match="any">
              <text macro="legal-cites"/>
            </if>
            <else>
              <text macro="legal-cites" suffix="."/>
            </else>
          </choose>
        </if>
        <else>
          <group delimiter=" ">
            <group delimiter=" ">
              <text macro="author-bib"/>
              <text macro="date-bib"/>
              <text macro="title-and-descriptions"/>
              <text macro="container"/>
              <text macro="event"/>
              <text macro="publisher"/>
            </group>
            <text macro="access"/>
            <text macro="publication-history"/>
          </group>
        </else>
      </choose>
    </layout>
  </bibliography>
</style>

