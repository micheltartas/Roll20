# Macros - Roll20
Esta é uma lista com alguns macros que podem ser utilizados no WebApp Roll20 para jogos de RPG . 
Sinta-se livre para utiliza-los em jogos! Bom jogo e divirta-se! :D

## Macros para Players (Jogadores)

### Ativar / Desativar o teste de Macros
Esta opção permite que você teste os seus macros sem que os outros (jogadores e mestre) recebam o que esta sendo digitado no Chat.
- Ativar: 		```/talktomyself on```
- Desativar:	```/talktomyself off``` 

## Iniciativa

Para que este macro funcione corretamente, você deve clicar (selecionar) o token desejado e utilizar o macro. Sua iniciativa será calculada automaticamente e colocada no Tracker de iniciativa automaticamente:

- ```&{template:default}  {{name= NOME_DO_JOGADOR Rola a Iniciativa}} {{Iniciativa=[[1d20 + 2 &{tracker}]]}}```


[[@{Austin Berevan|initiative_style}+@{Austin Berevan|initiative_bonus}@{Austin Berevan|pbd_safe}[INIT] &{tracker}]]

&{template:simple} {{rname=^{init-u}}} {{name= NOME_DO_JOGADOR Rola a Iniciativa}} {{r1=[[@{NOME_DO_PERSONAGEM|initiative_style}+@{NOME_DO_PERSONAGEM|initiative_bonus}@{NOME_DO_PERSONAGEM|pbd_safe}[INIT] &{tracker}]]}}

Este é um macro mais completo, ele adiciona o 
- ```@{NOME_DO_PERSONAGEM|wtype}&{template:simple} {{rname=^{init-u}}} {{mod=@{NOME_DO_PERSONAGEM|initiative_bonus}}} {{r1=[[@{NOME_DO_PERSONAGEM|initiative_style}+@{NOME_DO_PERSONAGEM|initiative_bonus}@{NOME_DO_PERSONAGEM|pbd_safe}[INIT] &{tracker}]]}} {{normal=1}} @{NOME_DO_PERSONAGEM|charname_output}```

> Exemplo: 
```@{Kaladan Ophinshtalajiir|wtype}&{template:default} {{rname=^{init-u}}} {{mod=@{Kaladan Ophinshtalajiir|initiative_bonus}}} {{r1=[[@{Kaladan Ophinshtalajiir|initiative_style}+@{Kaladan Ophinshtalajiir|initiative_bonus}@{Kaladan Ophinshtalajiir|pbd_safe}[INIT] &{tracker}]]}} {{normal=1}} @{Kaladan Ophinshtalajiir|charname_output}```

## Magias

<details>
	<summary>- Misseis Mágicos - Magic Missile</summary>

	```
	&{template:default} {{name=Mísseis Mágicos}} {{description= Acerta os alvos com [[?{Level cast at|1|2|3|4|5|6|7|8|9}+2]] Mísseis Mágicos.}} {{Damage= Dano Total: ?{Spell level?|

		 1, [[ [[1d4+1]]+[[1d4+1]]+[[1d4+1]] ]] Rolagens: ($[[0]] $[[1]] $[[2]])
		|2, [[ [[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]] ]] Rolagens: ($[[0]] $[[1]] $[[2]] $[[3]])
		|3, [[ [[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]] ]] Rolagens: ($[[0]] $[[1]] $[[2]] $[[3]] $[[4]])
		|4, [[ [[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]] ]] ToRolagenstal: ($[[0]] $[[1]] $[[2]] $[[3]] $[[4]] $[[5]])
		|5, [[ [[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]] ]] Rolagens: ($[[0]] $[[1]] $[[2]] $[[3]] $[[4]] $[[5]] $[[6]])
		|6, [[ [[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]] ]] Rolagens: ($[[0]] $[[1]] $[[2]] $[[3]] $[[4]] $[[5]] $[[6]] $[[7]])
		|7, [[ [[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]] ]] Rolagens: ($[[0]] $[[1]] $[[2]] $[[3]] $[[4]] $[[5]] $[[6]] $[[7]] $[[8]])
		|8, [[ [[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]] ]] Rolagens: ($[[0]] $[[1]] $[[2]] $[[3]] $[[4]] $[[5]] $[[6]] $[[7]] $[[8]] $[[9]])
		|9, [[ [[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]] ]] Rolagens: ($[[0]] $[[1]] $[[2]] $[[3]] $[[4]] $[[5]] $[[6]] $[[7]] $[[8]] $[[9]] $[[10]])
	}}}
	```
</details>

<details>
	<summary>- Mãos Flamejantes - Burning Hands</summary>

	```
	&{template:default} {{name=Mãos Flamejantes}} {{description= Acerta os alvos com um cone de fogo de 4,5m (15-foot cone)}} {{Damage= Dano Total: ?{Spell level?|

		 1, [[ [[1d6]]+[[1d6]]+[[1d6]] ]] Rolagens: ($[[0]] $[[1]] $[[2]])
		|2, [[ [[1d6]]+[[1d6]]+[[1d6]]+[[1d6]] ]] Rolagens: ($[[0]] $[[1]] $[[2]] $[[3]])
		|3, [[ [[1d6]]+[[1d6]]+[[1d6]]+[[1d6]]+[[1d6]] ]] Rolagens: ($[[0]] $[[1]] $[[2]] $[[3]] $[[4]])
		|4, [[ [[1d6]]+[[1d6]]+[[1d6]]+[[1d6]]+[[1d6]]+[[1d6]] ]] ToRolagenstal: ($[[0]] $[[1]] $[[2]] $[[3]] $[[4]] $[[5]])
		|5, [[ [[1d6]]+[[1d6]]+[[1d6]]+[[1d6]]+[[1d6]]+[[1d6]]+[[1d6]] ]] Rolagens: ($[[0]] $[[1]] $[[2]] $[[3]] $[[4]] $[[5]] $[[6]])
		|6, [[ [[1d6]]+[[1d6]]+[[1d6]]+[[1d6]]+[[1d6]]+[[1d6]]+[[1d6]]+[[1d6]] ]] Rolagens: ($[[0]] $[[1]] $[[2]] $[[3]] $[[4]] $[[5]] $[[6]] $[[7]])
		|7, [[ [[1d6]]+[[1d6]]+[[1d6]]+[[1d6]]+[[1d6]]+[[1d6]]+[[1d6]]+[[1d6]]+[[1d6]] ]] Rolagens: ($[[0]] $[[1]] $[[2]] $[[3]] $[[4]] $[[5]] $[[6]] $[[7]] $[[8]])
		|8, [[ [[1d6]]+[[1d6]]+[[1d6]]+[[1d6]]+[[1d6]]+[[1d6]]+[[1d6]]+[[1d6]]+[[1d6]]+[[1d6]] ]] Rolagens: ($[[0]] $[[1]] $[[2]] $[[3]] $[[4]] $[[5]] $[[6]] $[[7]] $[[8]] $[[9]])
		|9, [[ [[1d6]]+[[1d6]]+[[1d6]]+[[1d6]]+[[1d6]]+[[1d6]]+[[1d6]]+[[1d6]]+[[1d6]]+[[1d6]]+[[1d6]] ]] Rolagens: ($[[0]] $[[1]] $[[2]] $[[3]] $[[4]] $[[5]] $[[6]] $[[7]] $[[8]] $[[9]] $[[10]])
	}}}
	```
</details>



[[@{Austin Berevan|initiative_style}+@{Austin Berevan|initiative_bonus}@{Austin Berevan|pbd_safe}[INIT] &{tracker}]]}}






# Daqui pra baixo só teste e exemplos

@{Kaladan Ophinshtalajiir|wtype}&{template:atk} {{mod=+4}} {{rname=[Dagger](~-Mv1OVkz53Sy75PotA6B|repeating_attack_-Mv5f0MM4dMTaXwCis1j_attack_dmg)}} {{rnamec=[Dagger](~-Mv1OVkz53Sy75PotA6B|repeating_attack_-Mv5f0MM4dMTaXwCis1j_attack_crit)}} {{r1=[[@{Kaladan Ophinshtalajiir|d20}cs>20 + 2[DEX] + 2[PROF]]]}} @{Kaladan Ophinshtalajiir|rtype}cs>20 + 2[DEX] + 2[PROF]]]}} {{range=20/60}} {{desc=}} {{spelllevel=}} {{innate=}} {{globalattack=@{Kaladan Ophinshtalajiir|global_attack_mod}}} ammo= @{Kaladan Ophinshtalajiir|charname_output}


@{Kaladan Ophinshtalajiir|wtype}&{template:simple} {{rname=^{strength-u}}} {{mod=@{Kaladan Ophinshtalajiir|strength_mod}@{Kaladan Ophinshtalajiir|jack_bonus}}} {{r1=[[@{Kaladan Ophinshtalajiir|d20}+@{Kaladan Ophinshtalajiir|strength_mod}@{Kaladan Ophinshtalajiir|jack_attr}[STR]]]}} @{Kaladan Ophinshtalajiir|rtype}+@{Kaladan Ophinshtalajiir|strength_mod}@{Kaladan Ophinshtalajiir|jack_attr}[STR]]]}} @{Kaladan Ophinshtalajiir|charname_output}

@{NOME_DO_PERSONAGEM|ATRIBUTO_DESEJADO}
@{Kaladan Ophinshtalajiir|survival_roll}
@{Kaladan Ophinshtalajiir|inspiration}

inspiration

Kaladan Ophinshtalajiir


Exemplos:


# A collapsible section with markdown
<details>
  <summary>Click to expand!</summary>
  
  ## Heading
  1. A numbered
  2. list
     * With some
     * Sub bullets
</details>



## Daqui pra baixo é só teste
Total damage is: [[[[1d4+1]]*?{Level cast at}]] Each missile does $[[0]] force damage.

Macros:
 
→ Iniciativa:
	&{template:default}  {{name= Austin Berevan Rola a Iniciativa}} {{Iniciativa=[[1d20 + 2 &{tracker}]]}} 
	
→ Magic Missile	
	/em Acerta os alvos com [[?{Level cast at|1|2|3|4|5|6|7|8|9}+2]] Mísseis Mágicos. O Dano total é: [[[[1d4+1]]*?{Level cast at} * 2]] Each missile does $[[0]] force damage.
	/em Acerta os alvos com [[?{Level cast at|1|2|3|4|5|6|7|8|9}+2]] Mísseis Mágicos. O Dano total é: [[[[1d4+1]]*?{Level cast at} * 2]] Each missile does $[[0]] force damage.

	/em Acerta os alvos com [[?{Level cast at|1|2|3|4|5|6|7|8|9}+2]] Mísseis Mágicos. O Dano total é: [[[[1d4+1]]*{2+?{Level cast at}}]]. 




Nível da Magia 


?{Spell level?|

 1, [[ [[1d4+1]]+[[1d4+1]]+[[1d4+1]] ]] Total ($[[0]] $[[1]] $[[2]])
|2, [[ [[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]] ]] Total ($[[0]] $[[1]] $[[2]] $[[3]])
|3, [[ [[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]] ]] Total ($[[0]] $[[1]] $[[2]] $[[3]] $[[4]])
|4, [[ [[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]] ]] Total ($[[0]] $[[1]] $[[2]] $[[3]] $[[4]] $[[5]])
|5, [[ [[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]] ]] Total ($[[0]] $[[1]] $[[2]] $[[3]] $[[4]] $[[5]] $[[6]])
|6, [[ [[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]] ]] Total ($[[0]] $[[1]] $[[2]] $[[3]] $[[4]] $[[5]] $[[6]] $[[7]])
|7, [[ [[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]] ]] Total ($[[0]] $[[1]] $[[2]] $[[3]] $[[4]] $[[5]] $[[6]] $[[7]] $[[8]])
|8, [[ [[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]] ]] Total ($[[0]] $[[1]] $[[2]] $[[3]] $[[4]] $[[5]] $[[6]] $[[7]] $[[8]] $[[9]])
|9, [[ [[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]] ]] Total ($[[0]] $[[1]] $[[2]] $[[3]] $[[4]] $[[5]] $[[6]] $[[7]] $[[8]] $[[9]] $[[10]])

}


## Austin Berevan
### Fist
- Acerto:	[[1d20+9]]
- Dano:		[[3d10+6]]

### Rock
- Acerto	[[1d20+9]]
- Dano:		[[7d6+6]]


&{template:default} {{title=Magic Missile}}  {{attack_damage= ?{Spell level?
	|1, [[ [[1d4+1]]+[[1d4+1]]+[[1d4+1]] ]] Total ($[[0]] $[[1]] $[[2]])
	|2, [[ [[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]] ]] Total ($[[0]] $[[1]] $[[2]] $[[3]])
	|3, [[ [[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]] ]] Total ($[[0]] $[[1]] $[[2]] $[[3]] $[[4]])
	|4, [[ [[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]] ]] Total ($[[0]] $[[1]] $[[2]] $[[3]] $[[4]] $[[5]])
	|5, [[ [[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]] ]] Total ($[[0]] $[[1]] $[[2]] $[[3]] $[[4]] $[[5]] $[[6]])
	|6, [[ [[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]] ]] Total ($[[0]] $[[1]] $[[2]] $[[3]] $[[4]] $[[5]] $[[6]] $[[7]])
	|7, [[ [[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]] ]] Total ($[[0]] $[[1]] $[[2]] $[[3]] $[[4]] $[[5]] $[[6]] $[[7]] $[[8]])
	|8, [[ [[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]] ]] Total ($[[0]] $[[1]] $[[2]] $[[3]] $[[4]] $[[5]] $[[6]] $[[7]] $[[8]] $[[9]])
	|9, [[ [[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]] ]] Total ($[[0]] $[[1]] $[[2]] $[[3]] $[[4]] $[[5]] $[[6]] $[[7]] $[[8]] $[[9]] $[[10]])
}}}


&{template:default} {{title=Magic Missile}} {{spell=1}} {{spell_first_line=1}} {{spell_level=^{1ST_LEVEL}}} {{school=^{EVOCATION}}}  {{casting_time=^{1_ACTION}}} {{range=120 feet}} {{components=^{COMPONENTS_V_S}}} {{materials=}} {{duration=^{INSTANTANEOUS}}} {{content=You create three glowing darts of magical force. Each dart hits a creature of your choice that you can see within range. A dart deals 1d4 + 1 force damage to its target. The darts all strike simultaneously, and you can direct them to hit one creature or several.**}}  {{higher_level=At Higher Levels.** When you cast this spell using a spell slot of 2nd level or higher, the spell creates one more dart for each slot level above 1st.}} {{attack_damage_type=force}} {{has_attack_damage=1}}  {{attack_damage= ?{Spell level?|

1, [[ [[1d4+1]]+[[1d4+1]]+[[1d4+1]] ]] Total ($[[0]] $[[1]] $[[2]])
|2, [[ [[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]] ]] Total ($[[0]] $[[1]] $[[2]] $[[3]])
|3, [[ [[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]] ]] Total ($[[0]] $[[1]] $[[2]] $[[3]] $[[4]])
|4, [[ [[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]] ]] Total ($[[0]] $[[1]] $[[2]] $[[3]] $[[4]] $[[5]])
|5, [[ [[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]] ]] Total ($[[0]] $[[1]] $[[2]] $[[3]] $[[4]] $[[5]] $[[6]])
|6, [[ [[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]] ]] Total ($[[0]] $[[1]] $[[2]] $[[3]] $[[4]] $[[5]] $[[6]] $[[7]])
|7, [[ [[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]] ]] Total ($[[0]] $[[1]] $[[2]] $[[3]] $[[4]] $[[5]] $[[6]] $[[7]] $[[8]])
|8, [[ [[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]] ]] Total ($[[0]] $[[1]] $[[2]] $[[3]] $[[4]] $[[5]] $[[6]] $[[7]] $[[8]] $[[9]])
|9, [[ [[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]]+[[1d4+1]] ]] Total ($[[0]] $[[1]] $[[2]] $[[3]] $[[4]] $[[5]] $[[6]] $[[7]] $[[8]] $[[9]] $[[10]])

}}}