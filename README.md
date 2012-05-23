This is Viking - The ruthless build system

Viking is an opinionated set of build scripts based on ant 1.8,
meaning that it requires ant 1.8 to be operational. All other features
used by Viking are automatically downloaded when needed.

Build scripts can be hairy. Viking keeps all of the hair to itself,
making your build scripts short and clean, clear of gnarly details and
beard.

Your build script when using Viking is a minimal bootstrap portion
(copy from sample usage sectio below) to include the Viking build
scripts in your build, followed by using elements declaring the
features used by your build. These will hook in to the build phases of
Viking and work seamlessly to build your project.

Default usage:

    <project name="..." default="complete">
      <property name="viking.xml" location="build/viking.xml"/>
      <available file="${commons.xml}" property="commons.url"
                 value="file:${commons.xml}"/>
      <property name="commons.url" value="https://raw.github.com/thobe/viking/master/viking.xml"/>
      <import><url url="${commons.url}"/></import>

      <!-- any <using lib="..."/> goes here -->

    </project>

Note that the default target of a Viking build is always "complete",
and generally you should not need to build any other target.

Pro-tip: Viking works best with the following alias (bash syntax):

    alias taunt=ant

This allows you to taunt your build into submission like a true viking!
