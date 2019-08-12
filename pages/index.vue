<template>
  <v-layout column justify-center align-center>
    <v-container grid-list-xs fluid>
      <v-img
        class="img white--text"
        src="https://firebasestorage.googleapis.com/v0/b/app-safety.appspot.com/o/city.png?alt=media&token=76addadc-5820-4698-82c7-5c85264e68fe"
      >
        <v-container fill-height fluid>
          <v-layout fill-height>
            <v-flex xs12 md6 align-end flexbox>
              <span class="display-3 accent"
                >Reporta delitos en tu distrito anónimante...
              </span>
              <h2><span class="display-2 accent">¡Serás notificado! </span></h2>
            </v-flex>
          </v-layout>
        </v-container>
      </v-img>
    </v-container>
    <!-- <v-flex class="primary"></v-flex>
    <v-flex class="accent"></v-flex>
    <v-flex class="secondary"></v-flex>
    <v-flex class="info"></v-flex>
    <v-flex class="warning"></v-flex>
    <v-flex class="error"></v-flex>
    <v-flex class="success"></v-flex> -->

    <!-- <v-container grid-list-md>
      <v-layout row wrap>
        <v-flex class="primary"></v-flex>
        <v-flex class="accent"></v-flex>
        <v-flex class="secondary"></v-flex>
        <v-flex class="info"></v-flex>
        <v-flex class="warning"></v-flex>
        <v-flex class="error"></v-flex>
        <v-flex class="success"></v-flex>

        <v-flex md6>
          <h1>
            Reporta delitos en tu distrito anónimante.. ¡Serás notificado¡
          </h1>
        </v-flex>
      </v-layout>
    </v-container> -->
    <v-container grid-list-md>
      <v-layout row wrap>
        <v-flex md12 pa-4 ma-4>
          <h1 class="font-weight-regular accent--text">
            INCIDENTES QUE PUEDES REPORTAR
          </h1>
          <h2 class="font-weight-regular secondary--text">
            La plataforma te permite reportar diversos delitos
          </h2>
        </v-flex>
        <Incident image="ss" title="Robo a mano armada" lorem=" " />
        <Incident image="ss" title="Asaltos" lorem=" " />
        <Incident image="ss" title="Robo agravado" lorem=" " />
        <Incident image="ss" title="Venta de drogas" lorem=" " />
      </v-layout>
    </v-container>

    <!-- <v-container grid-list-md>
      <v-layout row wrap pa-4>
        <v-flex xs12 md12 pa-4 ma-2>
          <h3 class="display-1 font-weight-regular text-md-center">Precios</h3>
        </v-flex>
        <v-flex xs12 md2 />
        <Price :price="50.0" title="Precio 1" />
        <v-flex md2 />
        <Price :price="50.0" title="Precio 1" />
        <v-flex xs12 md2 />
      </v-layout>
    </v-container> -->

    <v-container class="accent" fluid py-5 mt-5>
      <v-container grid-list-md>
        <v-layout row wrap>
          <v-flex xs12 sm12 md12 pa-4 ma-2>
            <h3
              class="display-1 font-weight-regular white--text text-md-center"
            >
              ¿Preguntas frecuentes?
            </h3>
            <br />
          </v-flex>
          <Question
            question="¿Cómo envío una alerta?"
            response="Cuando se encuentre en una emergencia, solo tiene que presionar el botón SOS durante 3 segundos y su alerta será enviada"
          />
          <Question
            question="¿Qué son los ayudantes?"
            response="Los usuarios que ayudan han decidido que quieren ayudar a otros en caso de emergencias. Cuando un usuario envía una alerta, los ayudantes cercanos son notificados automáticamente de la situación. Los que puedan ayudar aceptarán su alerta y se dirigirán a su ubicación para brindarle ayuda de inmediato. Cualquier usuario puede convertirse en un ayudante. ¡Realmente lo alentamos a que también sea un ayudante y haga que nuestra comunidad sea más segura!"
          />
          <Question
            question="Quién recibira mi alerta"
            response="Sus contactos de emergencia serán notificados inmediatamente cuando envíe una alerta. Si son usuarios de WeHelp! serán notificados a través de una Notificación Push. Si no tienen la aplicación serán notificados a través de SMS. Los ayudantes cercanos también recibirán su alerta y lo ayudarán de inmediato."
          />
          <Question
            question="¿Cómo envío una alerta?"
            response="Cuando se encuentre en una emergencia, solo tiene que presionar el botón SOS durante 3 segundos y su alerta será enviada"
          />
        </v-layout>
      </v-container>
    </v-container>

    <v-container grid-list-md py-5 my-5>
      <v-layout row wrap>
        <v-flex md12 pa-4 ma-4>
          <h1 class="font-weight-regular accent--text">EQUIPO DE PROYECTO</h1>
          <h2 class="font-weight-regular secondary--text">
            Nuestra gente es lo que hace que todo suceda.
          </h2>
        </v-flex>
        <Team
          name="Erikson Daniel"
          position="Software Engineering"
          user="@eriksondaniel"
        />
        <Team
          name="Enzo Lizama"
          position="Software Engineering"
          user="@enzoftware"
        />
        <Team
          name="Luciana Montoya"
          position="Marketing"
          user="@lucianamontoya"
        />
        <Team name="Luis Pachas" position="Marketing" user="@luispachas" />
      </v-layout>
    </v-container>

    <v-container grid-list-md fluid class="secondary" py-5>
      <v-layout row wrap>
        <v-flex xs12 sm12 md12 my-2>
          <h3 class="display-1 font-weight-regular white--text text-md-center">
            Elige un plan y mantente seguro
          </h3>
          <br />
        </v-flex>
        <v-flex md2> </v-flex>
        <v-flex xs12 sm12 md8>
          <v-card flat class="accent">
            <v-card-title>
              <v-spacer></v-spacer>
              <h3 class="white--text">Premium</h3>
            </v-card-title>
            <template>
              <v-data-table :items="desserts" hide-actions hide-headers>
                <template v-slot:items="props">
                  <td class="font-weight-regular subheading accent white--text">
                    {{ props.item.name }}
                  </td>
                  <!-- <td class="text-xs-right accent">
                    <v-icon class="white--text">{{ props.item.check1 }}</v-icon>
                  </td>
                  <td class="text-xs-right accent">
                    <v-icon class="white--text">{{ props.item.check2 }}</v-icon>
                  </td> -->
                  <td class="text-xs-right accent">
                    <v-icon class="white--text">{{ props.item.check3 }}</v-icon>
                  </td>
                </template>
              </v-data-table>
            </template>
          </v-card>
        </v-flex>
        <v-flex md2> </v-flex>
      </v-layout>
    </v-container>
    <v-container fluid class="white">
      <v-container grid-list-md>
        <v-layout row wrap justify-center align-center>
          <v-flex md7 pa-4>
            <h2 class="display-1 font-weight-regular">
              Reporte delitos anonimamente
            </h2>
            <br />
            <h2 class="font-weight-regular">
              Descarga la aplicación Safety hoy
            </h2>
            <h2 class="font-weight-regular">
              Siéntase seguro en cualquier lugar, en cualquier momento.
            </h2>
          </v-flex>
          <v-flex md></v-flex>
          <v-flex md2 pa-3>
            <img src="~/assets/images/google-play.png" alt width="150" />
          </v-flex>
          <v-flex md2 pa-3>
            <img src="~/assets/images/app-store.svg" alt width="120" />
          </v-flex>
        </v-layout>
      </v-container>
    </v-container>
  </v-layout>
</template>

<script>
import Team from '@/components/Team'
import Incident from '@/components/Incident'
import Question from '@/components/Question'

export default {
  components: {
    Team,
    Incident,
    Question
  },
  data() {
    return {
      desserts: [
        {
          name: 'Precio mensual de que terminen los 15 días de prueba',
          check1: 'check',
          check2: 'check',
          check3: 'check'
        },
        {
          name: 'Acceso a datos de localización de zonas rojas',
          check1: 'check',
          check2: 'check',
          check3: 'check'
        },
        {
          name: 'Acceso a boton alerta SOS',
          check1: 'check',
          check2: 'check',
          check3: 'check'
        },
        {
          name: 'Visualización de publicaciones en tiempo real',
          check1: 'check',
          check2: 'check',
          check3: 'check'
        },
        {
          name:
            'Recibir/enviar fotos y mensajes de otros contactos en forma remota',
          check1: 'check',
          check2: 'check',
          check3: 'check'
        },
        {
          name: 'Realizar denuncias de una serie de incidentes',
          check1: 'check',
          check2: 'check',
          check3: 'check'
        },
        {
          name: 'Servicio de asistencia personalizada',
          check1: 'check',
          check2: 'check',
          check3: 'check'
        },
        {
          name: 'Primeros 15 días',
          check1: 'check',
          check2: 'check',
          check3: 'check'
        },
        {
          name: 'Cancelar en cualquier momento',
          check1: 'check',
          check2: 'check',
          check3: 'check'
        }
      ]
    }
  }
}
</script>
<style>
img {
  max-width: 100%;
  height: auto;
  /* width: auto\9; */
}

.vimg {
  max-width: 100%;
  height: auto;
}

.card-rounder {
  border-radius: 0.8rem;
}
</style>
