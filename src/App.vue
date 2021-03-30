<template>
    <div class="wrapper">
        <the-header/>

        <div class="content">
            <h2 class="content__title">Career Timeline</h2>

            <ul class="career-list">

                <li
                        v-for='(item, index) in carrerList'
                        :key="index"
                        class="career-item"
                >
                    <div class="career-item__left">
                        <p class="career-item__name">{{ item.name }}</p>
                        <span class="career-item__company">{{ item.company }}</span>
                    </div>
                    <div class="career-item__right">
                        <span class="career-item__address">{{ item.address }}</span>
                        <span class="career-item__date">{{ item.date }}</span>
                    </div>
                    <i class="fas fa-caret-left"></i>
                </li>
            </ul>
        </div>

        <the-footer/>
    </div>
</template>

<script>
    import TheHeader from './components/TheHeader';
    import TheFooter from './components/TheFooter';

    export default {
        name: 'App',

        components: {
            TheHeader,
            TheFooter,
        },

        data() {
            return {
                carrerList: [
                    {
                        name: 'Freelance Web UI Designer &amp; Developer',
                        companyName: 'at Web Cream (webcream.ca)',
                        address: 'Montreal, Canada.',
                        date: 'Feb 2013 - Present',
                    },
                    {
                        name: 'Comprehensive Project Management Course',
                        companyName: 'at School of continuing studies, McGill University.',
                        address: 'Montreal, Canada.',
                        date: 'Sep 2012 - Mar 2013',
                    },
                    {
                        name: 'Webmaster',
                        companyName: 'at Doctors Without Borders, Middle East regional office (msf-me.org)',
                        address: 'Abu Dhabi, UAE.',
                        date: 'Dec 2009 - Jun 2012',
                    },
                    {
                        name: 'Web UI Designer & Developer',
                        companyName: 'at School of continuing studies, McGill University.',
                        address: 'Dubai, UAE.',
                        date: 'Dec 2008 - Dec 2009',
                    },
                    {
                        name: 'Front-end Developer',
                        companyName: 'at Catch Interactive',
                        address: 'Dubai, UAE.',
                        date: 'Jan 2008 - Dec 2008',
                    },
                    {
                        name: 'CIW Professional Certification',
                        companyName: 'at ciwcertified.com',
                        address: 'Oct 2007',
                        date: '',
                    },
                    {
                        name: 'Web Designer',
                        companyName: 'at Victory Link (victorylink.com)',
                        address: 'Cairo, Egypt.',
                        date: 'Sep 2005 - Oct 2007',
                    },
                    {
                        name: 'B.Sc., Computer Engineering',
                        companyName: 'at AIET',
                        address: 'Alexandria, Egypt.',
                        date: 'Aug 2005',
                    },
                ]
            }
        }
    }
</script>

<style lang="scss">
    * {
        padding: 0;
        margin: 0;
        box-sizing: border-box;
    }

    .wrapper {
        font-family: 'Open Sans', sans-serif;
        font-size: 10px;
        background-color: #fff;
        max-width: 550px;
        margin-right: auto;
        margin-left: auto;
        padding: 0 10px;
    }

    .contacts {
        margin: 20px 0;
    }

    ul li {
        list-style: none;
    }

    .contact-list {
        display: flex;
        justify-content: space-between;
        align-items: center;
    }

    .fas {
        color: #e74c3c;
    }

    .contact-item__link {
        text-decoration: none;
        color: #34495e;
        font-weight: 100;
        transition: color 0.3s linear;
    }

    .contact-item__link:hover {
        color: #e74c3c;
    }

    .content {
        margin-bottom: 30px;
    }

    .content__title {
        font-family: 'Roboto Slab', serif;
        font-weight: 100;
        font-size: 14px;
        color: #fff;
        background-color: #34495e;
        padding: 7px;
        border-radius: 5px;
        margin-bottom: 25px;
    }

    .career-list {
        position: relative;
    }

    .career-list::before {
        content: '';
        position: absolute;
        left: 50%;
        top: 25px;
        bottom: 25px;
        transform: translateX(-50%);
        width: 2px;
        background-color: #e74c3c;
    }

    .career-item {
        display: flex;
        position: relative;
        color: #fff;
        width: 245px;
    }

    .career-item i {
        position: absolute;
        left: 99%;
        top: 10px;
        font-size: 20px;
    }

    .career-item::after {
        position: absolute;
        content: '';
        top: 12px;
        right: -11%;
        width: 10px;
        height: 10px;
        border-radius: 50%;
        border: 2px solid #e74c3c;
        background-color: #fff;
    }

    .career-item:nth-child(even) {
        margin-left: auto;
        margin-bottom: 15px;
    }

    .career-item:nth-child(even)::after {
        left: -11%;
    }


    .career-item:nth-child(even) i {
        color: #34495e;
        left: auto;
        right: 99%;
    }

    .career-item__left {
        width: 155px;
        padding: 7px;
        border-radius: 5px 0 0 5px;
        background-color: #34495e;
    }

    .career-item__company {
        font-weight: 300;
        font-style: italic;
        font-size: 8px;
    }

    .career-item__address {
        display: block;
    }

    .career-item__right {
        width: 88px;
        padding: 7px;
        border-radius: 0 5px 5px 0;
        background-color: #e74c3c;
    }

    .career-item__address {
        font-size: 8px;
        font-style: italic;
    }

    .career-item__date {
        font-size: 7px;
    }

    @media (max-width: 550px) {
        .header__title {
            font-size: 28px;
        }

        .career-item {
            justify-content: center;
            width: auto;
            margin-bottom: 10px;
        }

        .career-item i,
        .career-list::before,
        .career-item::after {
            display: none;
        }

        .career-item__left {
            width: 70%;
        }
        .career-item__right {
            width: 30%;
        }

        .career-item:nth-child(even) {
            margin-bottom: 10px;
        }

        .footer {
            flex-direction: column;
            align-items: center;
        }

        .footer__col {
            width: 100%;
        }
    }

    @media (max-width: 480px) {
        .header {
            flex-direction: column;
        }

        .career-item__name {
            font-size: 12px;
        }

        .career-item__company {
            font-size: 10px;
        }

        .career-item__address {
            font-size: 10px;
        }

        .career-item__date {
            font-size: 9px;
        }
    }

    @media (max-width: 440px) {
        .contact-item {
            display: flex;
            align-items: center;
            flex-direction: column;
        }
    }

    @media (max-width: 390px) {
        .contacts {
            margin: 10px 0;
        }
        .contact-list {
            flex-direction: column;
        }

        .contact-item:not(:nth-child(4)) {
            margin-bottom: 10px;
        }

        .content__title,
        .footer__title {
            text-align: center;
        }
    }
</style>
