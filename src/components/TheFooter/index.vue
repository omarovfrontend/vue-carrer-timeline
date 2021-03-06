<template>
    <footer class="footer">
        <footer-menu
                class="footer__col"
                title="Skillset"
                :menu="leftMenu"
        />
        <footer-menu
                class="footer__col"
            title="Toolbox"
            :menu="rightMenu"
        />
    </footer>
</template>

<script>
    import FooterMenu from './FooterMenu';

    export default {
        name: 'TheFooter',
        components: {
            FooterMenu,
        },

        data() {
            return {
                leftMenu: [
                    {
                        link: '#',
                        name: 'Responsive Web Design'
                    },
                    {
                        link: '#',
                        name: 'UI/UX Design'
                    },
                    {
                        link: '#',
                        name: 'UI Development'
                    },
                    {
                        link: '#',
                        name: 'Information Architecture'
                    },
                    {
                        link: '#',
                        name: 'Prototyping'
                    },
                    {
                        link: '#',
                        name: 'Project Managment'
                    },
                    {
                        link: '#',
                        name: 'CMS Management'
                    },
                    {
                        link: '#',
                        name: 'Email List Managment'
                    },
                    {
                        link: '#',
                        name: 'Web Hosting Managment'
                    },
                    {
                        link: '#',
                        name: 'SEO'
                    }
                ],
                rightMenu: [
                    {
                        link: '#',
                        name: 'Adobe Photoshop'
                    },
                    {
                        link: '#',
                        name: 'Adobe Illustrator'
                    },
                    {
                        link: '#',
                        name: 'Adobe Dreamweaver'
                    },
                    {
                        link: '#',
                        name: 'Aptana Studio'
                    },
                    {
                        link: '#',
                        name: 'HTML, CSS, jQuery'
                    },
                    {
                        link: '#',
                        name: 'WordPress'
                    },
                    {
                        link: '#',
                        name: 'Bootstrap'
                    },
                    {
                        link: '#',
                        name: 'WAMP'
                    },
                    {
                        link: '#',
                        name: 'Plesk, cPanel'
                    },
                    {
                        link: '#',
                        name: 'Filezilla'
                    }
                ]
            }
        }
    }
</script>

<style lang="scss" scoped>
    .footer {
        display: flex;
        justify-content: space-between;
        margin-bottom: 50px;

        &__col {
            width: 47%;
            margin-bottom: 20px;
        }
    }
</style>