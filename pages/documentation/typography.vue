<template>
  <main class="site-main">
    <div class="content">
      <h1>Heading</h1>
      <p>
        To create header use tag heading
        <code class="label">(h1, h2,..., h6)</code> or use as class inside your
        element tag.
      </p>
      <h1>Heading 1</h1>
      <h2>Heading 2</h2>
      <h3>Heading 3</h3>
      <h4>Heading 4</h4>
      <h5>Heading 5</h5>
      <h6>Heading 6</h6>
      <div class="code-group">
        <code v-for="i in 6" :key="i">
          &lt;h{{ i }}&gt; Heading {{ i }} &lt;/h{{ i }}&gt; <br />
        </code>
      </div>

      <p class="h1">Heading 1</p>
      <p class="h2">Heading 2</p>
      <p class="h3">Heading 3</p>
      <p class="h4">Heading 4</p>
      <p class="h5">Heading 5</p>
      <p class="h6">Heading 6</p>
      <div class="code-group">
        <code v-for="i in 6" :key="i">
          &lt;h{{ i }} class="h{{ i }}"&gt; Heading {{ i }} &lt;/h{{ i }}&gt;
          <br />
        </code>
      </div>

      <h1>Text Style</h1>
      <p class="font--bold">Font Bold</p>
      <code class="label">
        &lt;p class="font--bold&gt; Font Bold &lt;/p&gt;
      </code>
      <p class="font--semi-bold">Font Semi Bold</p>
      <code class="label">
        &lt;p class="font--semi-bold&gt; Font Semi Bold &lt;/p&gt;
      </code>
      <p class="text--overline">Text Overline</p>
      <code class="label">
        &lt;p class="text--overline&gt; Text Overline &lt;/p&gt;
      </code>
      <p class="text--linetrough">Text Linetrough</p>
      <code class="label">
        &lt;p class="text--linetrough&gt; Text Linetroughd &lt;/p&gt;
      </code>
      <p class="text--underline">Text Underline</p>
      <code class="label">
        &lt;p class="text--underline&gt; Text Underline &lt;/p&gt;
      </code>
    </div>
  </main>
</template>

<script>
export default {
  name: 'DocsPage',
  data() {
    return {
      headerTag: '<h1>Heading 1</h1>'
    }
  }
}
</script>

<style lang="scss" scoped>
.site-main {
  width: 100%;
  background-color: #fafafa;
  display: flex;
  justify-content: center;
}

.content {
  width: 93%;
  padding: 70px 0 6em 0;

  @media #{$large} {
    padding-top: 100px;
    padding-left: 320px;
    padding-right: 320px;
  }
}

.label {
  padding: 2px 8px;
  border-radius: 5px;
  background-color: rgb(226, 233, 238);
  color: #3b3b3b;
  font-size: 0.9em;
}

.code-group {
  background-color: rgb(226, 233, 238);
  border-radius: 5px;
  padding: 1em 1em;
}
</style>
