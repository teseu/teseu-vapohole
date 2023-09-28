<script setup>
import Card from '@/components/ui/TheCard.vue'
 import Title from '@/components/ui/TheTitle.vue'
</script>

<template>
  <div class="flex flex-col mb-8">
    <div class="flex flex-col gap-4">
      <Title>
        <template #titulo>Dicas</template>
      </Title>
      <h2 class="text-3xl mb-4">Introdução</h2>
      <p class="text-base mb-4">
        Há diversas coisas para personalizar a interface do terminal e deixá-lo com a cara que vc quer,
        desde a escolha do emulador (são tantos e para tantos ambientes que fica difícil descrever) até a
        configuração oferecida por tal emulador.
      </p>
      <p class="text-base mb-4">
        Apesar de ser uma coisa que fiz muito, ainda faço, só que menos agora q tenho todos os meus emuladores já
        personalizados em algum ponto, ñ é o assunto proposto aqui nas dicas, até poderia fazer se sentisse q seria
        útil ou algo q o público dessa pág acha relevante.
      </p>
      <p class="text-base mb-4">
        Dito tudo isso, vou começar com os Prompt's, que usei o bash como exemplo, mas quase tudo é possível usar
        no fish tb. Digo quase tudo pq já me deparei com algumas exceções com o zsh pelo menos, principalmente ao
        usar o tmux, por isso, apesar de ter trocado pro zsh há algum tempo, o shell padrão do tmux no meu ambiente
        em casa é o bash.
      </p>
      <Card>
        <template #titulo>Interface</template>
        <h2 class="text-3xl mb-4">Prompt</h2>
        <p class="text-base mb-4">
          Na página About há alguns screenshots de como a tela ficou personalizando tanto o prompt qto o próprio tmux.
          Ali tem um pouco de tudo, um novo prompt, usando <a class="link" href="https://starship.rs/" target="_blank" >
            starship</a>, vários plugins para o tmux e alterações no .bashrc. Começando pelo prompt.
        </p>
        <p class="text-base mb-4">
          A instalação é bem simples do starship, de acordo com o sistema escolhido, sendo que para uso no vaporHole a opção é a
          instalação via curl, a 1ª q aparece se vc selecionar o Linux como sistema. A configuração depende muito de
          onde vc quer chegar, sendo q a personalização vc encontra dentro de <a class="link"
          href="https://starship.rs/presets/" target="_blank">Presets</a>. encontre o q mais se aproxima do q vc
          gosta e use, ou altere a seu gosto a partir de um desses.
        </p>
        <p class="text-base mb-4">Uma outra opção para personalizar o prompt é o <a class="link" href="https://github.com/ohmybash/oh-my-bash">Oh-My-Bash</a>, que pelo nome dá pra notar, é para uso no Bash, mas que tem versão para <a class="link" href="https://ohmyz.sh/">Zsh</a>, <a class="link" href="https://github.com/oh-my-fish/oh-my-fish">Fish</a> e até para <a class="link" href="https://ohmyposh.dev/">Power shell</a>, uma boa surpresa. São fáceis de instalar e configurar, a parte da personalização é bem simples e o tempo q leva só depende do quão longe se quer ir das opções padrão e por qual caminho (editando um arquivo pronto q mais se aproxima do desejado ou começando do zero depois de entender como alterar os parâmetros dos arquivos de configuração, os chamados dotfiles).</p>
        <h2 class="text-3xl mb-4 mt-8">O comando li</h2>
        <p class="text-base mb-2">O comando em si é um alias para:</p>
        <pre>'exa -lah --icons'</pre>
        <p class="text-base mb-4 mt-2">O comando <a class="link" href="https://the.exa.website/">exa</a>, como dito logo no início em seu site, se trata de um substituto moderno para o ls. Aceita as mesmas flags e tem algumas opções a mais.</p>
        <p class="text-base mb-4">Tenho usado há algum tempo e me sinto satisfeito com a mudança, uso com essas opções pq gosto das listagens longas (o 'l'), gosto de ver todos os arquivos (o 'a', de all), prefiro saber o tamanho dos arquivos em unidades mais fáceis de compreender (o 'h' de humano) e acho a exibição dos ícones (aqui é só do exa mesmo, o '--icons') na lista bem útil e tb mais bonita, pq ñ dizer, assim como o colorido da lista, q vc vai acostumando pra diferenciar certas coisas.</p>
        <h2 class="text-3xl mb-4 mt-8">Tmux</h2>
        <p class="text-base mb-4">
          O tmux é um pouco diferente, a customização q eu fiz depende da instalação de diversos plugins, e há várias
          formas de instalar cada um deles tb, assim como uma lista enorme para se escolher. Depois de procurar um
          pouco, descobri q a partir de um plugin, q basicamente serve para instalar e atualizar outros plugins, a
          tarefa seria bem mais leve do q inicialmente achava.
        </p>
        <p class="text-base mb-4">O plugin em questão é o <a class="link" href="https://github.com/tmux-plugins/tpm">Tmux Plugin Manager - TPM</a>, q mostra sua instalação, como instalar outros, exemplos e um <a class="link" href="https://github.com/tmux-plugins/list">link</a> com uma lista de plugins, com as mais variadas funcionalidades, para escolher, recomendo muito.</p>
      </Card>
      
    </div>
  </div>
</template>
<style scoped>

</style>
