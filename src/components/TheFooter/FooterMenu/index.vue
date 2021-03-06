<template>
    <div class="footer-menu">
        <h2 class="footer-menu__title">{{ title }}</h2>
        <ul class="footer-menu__list">
            <li
                    v-for='(item, index) in menu'
                    :key="index"
                    class="footer-menu__item"
            >
                <i class="fas fa-chevron-right"></i>
                <a class="footer-menu__link" :href="item.link">{{ item.name }}</a>
            </li>
        </ul>
    </div>
</template>

<script>
    export default {
        name: 'FooterMenu',

        props: {
            title: {
                type: String,
                default: '',
            },
            menu: {
                type: Array,
                default: () => []
            }
        }
    }
</script>

<style lang="scss" scoped>
    .footer-menu {
        &__title {
            font-family: 'Roboto Slab', serif;
            font-weight: 100;
            background-color: #34495e;
            color: #fff;
            padding: 7px;
            border-radius: 5px;
            margin-bottom: 15px;
        }

        &__list {
            column-count: 2;
            font-size: 9px;
        }

        &__link {
            padding-left: 5px;
            text-decoration: none;
            color: #34495e;
        }

        &__link:hover {
            text-decoration: underline;
        }
    }
</style>