<!--<template>-->
<!--	<nav>-->
<!--		<v-app-bar app class="teal">-->

<!--			<v-app-bar-nav-icon @click="drawer=!drawer">-->

<!--			</v-app-bar-nav-icon>-->

<!--			<v-toolbar-title>-->
<!--				<span class="font-weight-bold">旅游门票信息管理系统</span>-->
<!--				<span></span>-->
<!--			</v-toolbar-title>-->

<!--			<v-spacer>-->

<!--			</v-spacer>-->
<!--			<v-menu offset-y>-->
<!--				<template v-slot:activator="{ on, attrs }">-->
<!--					<v-btn  v-bind="attrs" v-on="on" text>-->
<!--						<span class="font-weight-bold">菜单</span>-->
<!--					</v-btn>-->
<!--				</template>-->
<!--				<v-list>-->
<!--					<v-list-item v-for="(item, index) in items" :key="index">-->
<!--						<v-list-item-title>{{ item.title }}</v-list-item-title>-->
<!--					</v-list-item>-->
<!--				</v-list>-->
<!--			</v-menu>-->
<!--			<v-btn text>-->
<!--				<span class="font-weight-bold">退出</span>-->
<!--				<v-icon>exit_to_app</v-icon>-->
<!--			</v-btn>-->
<!--		</v-app-bar>-->

<!--		<v-navigation-drawer color="#f8f8f8" app v-model="drawer">-->
<!--			<v-list>-->
<!--				<v-list-group prepend-icon="settings" no-action>-->
<!--					<template v-slot:activator>-->
<!--						<v-list-item-title>景区信息管理模块</v-list-item-title>-->
<!--					</template>-->
<!--					-->
<!--					<v-list-item>-->
<!--						<v-list-item-content>-->
<!--							权限管理-->
<!--						</v-list-item-content>-->
<!--					</v-list-item>-->
<!--					-->
<!--					-->
<!--					<v-list-item>-->
<!--						<v-list-item-content>-->
<!--							用户管理-->
<!--						</v-list-item-content>-->
<!--					</v-list-item>-->
<!--					-->
<!--					-->
<!--				</v-list-group>-->
<!--			</v-list>-->
<!--      <v-list>-->
<!--        <v-list-group prepend-icon="settings" no-action>-->
<!--          <template v-slot:activator>-->
<!--            <v-list-item-title>景区信息管理模块</v-list-item-title>-->
<!--          </template>-->

<!--          <v-list-item>-->
<!--            <v-list-item-content>-->
<!--              权限管理-->
<!--            </v-list-item-content>-->
<!--          </v-list-item>-->


<!--          <v-list-item>-->
<!--            <v-list-item-content>-->
<!--              用户管理-->
<!--            </v-list-item-content>-->
<!--          </v-list-item>-->


<!--        </v-list-group>-->
<!--      </v-list>-->

<!--		</v-navigation-drawer>-->
<!--	</nav>-->
<!--</template>-->

<!--<script>-->
<!--	export default {-->
<!--		data: function() {-->
<!--			return {-->
<!--				drawer: true,-->
<!--				items: [{-->
<!--						title: 'Click Me'-->
<!--					},-->
<!--					{-->
<!--						title: 'Click Me'-->
<!--					},-->
<!--					{-->
<!--						title: 'Click Me'-->
<!--					},-->
<!--					{-->
<!--						title: 'Click Me 2'-->
<!--					},-->
<!--				],-->
<!--			}-->
<!--		}-->
<!--	}-->
<!--</script>-->









<template>
  <v-app id="inspire">
    <v-app-bar
        app
        color=""
        flat
    >
      <v-container class="py-0 fill-height">
        <v-avatar
            class="mr-10"
            color="grey darken-1"
            size="32"
        ></v-avatar>

        <v-btn
            v-for="link in links"
            :key="link"
            text
        >
          {{ link }}
        </v-btn>

        <v-spacer></v-spacer>

        <v-responsive max-width="260">
          <v-text-field
              dense
              flat
              hide-details
              rounded
              solo-inverted
          ></v-text-field>
        </v-responsive>
      </v-container>
    </v-app-bar>

    <v-main class="grey lighten-3">
      <v-container>
        <v-row>
          <v-col cols="2">
            <v-sheet rounded="lg">
              <v-list dense>
                <v-subheader>REPORTS</v-subheader>
                <v-list-item-group
                    v-model="selectedItem"
                    color="primary"
                >
                  <v-list-item
                      v-for="(item, i) in items"
                      :key="i"
                  >
                    <v-list-item-icon>
                      <v-icon v-text="item.icon"></v-icon>
                    </v-list-item-icon>
                    <v-list-item-content>
                      <v-list-item-title v-text="item.text"></v-list-item-title>
                    </v-list-item-content>
                  </v-list-item>
                </v-list-item-group>
              </v-list>
            </v-sheet>
          </v-col>

          <v-col>
            <v-sheet
                min-height="70vh"
                rounded="lg"
            >
              <!--  -->
            </v-sheet>
          </v-col>
        </v-row>
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
export default {
  data: () => ({
    links: [
      '特色景区',
      '特色商品',

    ],
    selectedItem: 1,
    items: [
      { text: 'Real-Time', icon: 'mdi-clock' },
      { text: 'Audience', icon: 'mdi-account' },
      { text: 'Conversions', icon: 'mdi-flag' },
    ],
  }),
}
</script>
<style>
</style>
