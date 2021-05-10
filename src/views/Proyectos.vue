<template>
  <v-container
    id="proyectos"
    fluid
    tag="section"
  >
    <clientes />
    <v-data-table
      v-model="selected"
      :headers="headers"
      :items="desserts"
      :single-select="singleSelect"
      item-key="nombre"
      show-select
      class="elevation-1"
    >
      <template v-slot:top>
        <v-switch
          v-model="singleSelect"
          label="Selección única"
          class="pa-3"
        />
      </template>
      <v-pagination
        v-model="page"
        :length="15"
        :total-visible="7"
      />
    </v-data-table>
  </v-container>
</template>

<script>
  import Clientes from '../components/Clientes.vue'
  export default {
    name: 'Proyectos',
    components: { Clientes },
    data () {
      return {
        page: 1,
        singleSelect: false,
        selected: [],
        headers: [
          {
            text: 'Nombre',
            align: 'start',
            sortable: true,
            value: 'nombre',
          },
          { text: 'Código', value: 'codigo' },
          { text: 'Dirección', value: 'direccion' },
          { text: 'Empresa', value: 'empresa' },
          { text: 'Persona de contacto', value: 'contacto' },
          { text: 'Teléfono', value: 'telefono' },
        ],
        desserts: [
          {
            nombre: 'Franzen Venneur',
            codigo: 144,
            empresa: 'United Airlines',
            telefono: 124075168,
            direccion: 'Medford, Massachusetts, United States',
            contacto: 'Kenyon',
          },
          {
            nombre: 'Maggy Kibbey',
            codigo: 139,
            empresa: 'Stripe',
            telefono: 182761361,
            direccion: 'Springfield, Missouri, United States',
            contacto: 'Cristionna',
          },
          {
            nombre: 'Diannne Rawlingson',
            codigo: 111,
            empresa: 'Doist',
            telefono: 29559001,
            direccion: 'Hammond, Indiana, United States',
            contacto: 'Erhard',
          },
          {
            nombre: 'Josie Reasce',
            codigo: 6,
            empresa: 'PepsiCo',
            telefono: 19477085,
            direccion: 'Prescott Valley, Arizona, United States',
            contacto: 'Delphinia',
          },
          {
            nombre: 'Iolande Gisburn',
            codigo: 1,
            empresa: 'Kroger',
            telefono: 226264665,
            direccion: 'Wausau, Wisconsin, United States',
            contacto: 'Guinevere',
          },
          {
            nombre: 'Hershel Eagell',
            codigo: 22,
            empresa: 'Dropbox',
            telefono: 82919073,
            direccion: 'Medford, Oregon, United States',
            contacto: 'Charo',
          },
          {
            nombre: 'Rhianon Anten',
            codigo: 217,
            empresa: 'JP Morgan Chase',
            telefono: 207215283,
            direccion: 'Apopka, Florida, United States',
            contacto: 'Aleen',
          },
          {
            nombre: 'Antoine Hollyland',
            codigo: 47,
            empresa: 'FedEx',
            telefono: 120896939,
            direccion: 'Cedar Rapids, Iowa, United States',
            contacto: 'Katuscha',
          },
          {
            nombre: 'Etienne Strettell',
            codigo: 159,
            empresa: 'Palentir Technologies',
            telefono: 27751606,
            direccion: 'Shelton, Connecticut, United States',
            contacto: 'Seth',
          },
          {
            nombre: 'Pepito Boman',
            codigo: 72,
            empresa: 'Allstate',
            telefono: 144979497,
            direccion: 'Puyallup, Washington, United States',
            contacto: 'Heath',
          },
          {
            nombre: 'Aleen Keitley',
            codigo: 213,
            empresa: 'Ford Motor',
            telefono: 190370508,
            direccion: 'Blue Springs, Missouri, United States',
            contacto: 'Joyann',
          },
          {
            nombre: 'Caesar Scherme',
            codigo: 137,
            empresa: 'Dell Technologies',
            telefono: 182660342,
            direccion: 'Wylie, Texas, United States',
            contacto: 'Rodd',
          },
          {
            nombre: 'Hershel Ludron',
            codigo: 240,
            empresa: 'Allstate',
            telefono: 39485150,
            direccion: 'Pocatello, Idaho, United States',
            contacto: 'Costa',
          },
          {
            nombre: 'Way Hollyland',
            codigo: 236,
            empresa: 'Doist',
            telefono: 205383420,
            direccion: 'Lancaster, Pennsylvania, United States',
            contacto: 'Gayel',
          },
          {
            nombre: 'Alvinia Cassell',
            codigo: 173,
            empresa: 'CVS Health',
            telefono: 242352311,
            direccion: 'Muskegon, Michigan, United States',
            contacto: 'Anthe',
          },
          {
            nombre: 'Imogene Haighton',
            codigo: 133,
            empresa: 'Best Buy',
            telefono: 177628273,
            direccion: 'Racine, Wisconsin, United States',
            contacto: 'Ettie',
          },
          {
            nombre: 'Eugenius Mordy',
            codigo: 155,
            empresa: 'Chevron',
            telefono: 127535040,
            direccion: 'Duncanville, Texas, United States',
            contacto: 'Renata',
          },
          {
            nombre: 'King Gecks',
            codigo: 215,
            empresa: 'State Farm Insurance',
            telefono: 84012542,
            direccion: 'Newton, Massachusetts, United States',
            contacto: 'Jilly',
          },
          {
            nombre: 'Geno Worviell',
            codigo: 220,
            empresa: 'Postmates',
            telefono: 143484385,
            direccion: 'Moorhead, Minnesota, United States',
            contacto: 'King',
          },
          {
            nombre: 'Tersina McDiarmid',
            codigo: 59,
            empresa: 'Postmates',
            telefono: 237848045,
            direccion: 'Camarillo, California, United States',
            contacto: 'Erhart',
          },
          {
            nombre: 'Richardo Cathro',
            codigo: 217,
            empresa: 'Amazon',
            telefono: 203305793,
            direccion: 'Taunton, Massachusetts, United States',
            contacto: 'Halie',
          },
          {
            nombre: 'Katie Pidler',
            codigo: 229,
            empresa: 'Dell Technologies',
            telefono: 218544141,
            direccion: 'Methuen, Massachusetts, United States',
            contacto: 'Seth',
          },
          {
            nombre: 'Domini Durrett',
            codigo: 42,
            empresa: 'Allstate',
            telefono: 189631069,
            direccion: 'Murrieta, California, United States',
            contacto: 'Anita',
          },
          {
            nombre: 'Zaneta Whitsey',
            codigo: 79,
            empresa: 'JP Morgan Chase',
            telefono: 65525336,
            direccion: 'Morgan Hill, California, United States',
            contacto: 'Ernesto',
          },
          {
            nombre: 'Rickey Davidi',
            codigo: 48,
            empresa: 'Anthem',
            telefono: 70655964,
            direccion: 'Orange, California, United States',
            contacto: 'Tom',
          },
        ],
      }
    },
  }
</script>
