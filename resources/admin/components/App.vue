<template>
    <div>
        <div id="kt_header_mobile" class="kt-header-mobile  kt-header-mobile--fixed ">
            <div class="kt-header-mobile__logo">
                <router-link :to="{name: 'index'}">
                    <img alt="Logo" src="/dash/img/logo-light.png"/>
                </router-link>
            </div>
            <div class="kt-header-mobile__toolbar">
                <button class="kt-header-mobile__toggler kt-header-mobile__toggler--left" id="kt_aside_mobile_toggler">
                    <span></span></button>
                <button class="kt-header-mobile__toggler" id="kt_header_mobile_toggler"><span></span></button>
                <button class="kt-header-mobile__topbar-toggler" id="kt_header_mobile_topbar_toggler"><i
                        class="flaticon-more"></i></button>
            </div>
        </div>
        <div class="kt-grid kt-grid--hor kt-grid--root">
            <div class="kt-grid__item kt-grid__item--fluid kt-grid kt-grid--ver kt-page">
                <button class="kt-aside-close " id="kt_aside_close_btn"><i class="la la-close"></i></button>

                <div class="kt-aside  kt-aside--fixed  kt-grid__item kt-grid kt-grid--desktop kt-grid--hor-desktop"
                     id="kt_aside">

                    <div class="kt-aside__brand kt-grid__item " id="kt_aside_brand">
                        <div class="kt-aside__brand-logo">
                            <router-link tag="a" :to="{name: 'index'}">
                                <img alt="Logo" src="/dash/img/logo-light.png"/>
                            </router-link>
                        </div>
                    </div>

                    <div class="kt-aside-menu-wrapper kt-grid__item kt-grid__item--fluid" id="kt_aside_menu_wrapper">
                        <div id="kt_aside_menu" class="kt-aside-menu " data-ktmenu-vertical="1" data-ktmenu-scroll="1"
                             data-ktmenu-dropdown-timeout="500">
                            <ul class="kt-menu__nav ">
                                <li class="kt-menu__item" v-bind:class="{'kt-menu__item--active':(page === 'index')}"
                                    aria-haspopup="true">
                                    <router-link tag="a" :to="{name: 'index'}" class="kt-menu__link">
										<span class="kt-menu__link-icon">
											<svg xmlns="http://www.w3.org/2000/svg"
                                                 xmlns:xlink="http://www.w3.org/1999/xlink" width="24px" height="24px"
                                                 viewBox="0 0 24 24" version="1.1" class="kt-svg-icon">
												<g stroke="none" stroke-width="1" fill="none" fill-rule="evenodd">
													<polygon id="Bound" points="0 0 24 0 24 24 0 24"/>
													<path d="M12.9336061,16.072447 L19.36,10.9564761 L19.5181585,10.8312381 C20.1676248,10.3169571 20.2772143,9.3735535 19.7629333,8.72408713 C19.6917232,8.63415859 19.6104327,8.55269514 19.5206557,8.48129411 L12.9336854,3.24257445 C12.3871201,2.80788259 11.6128799,2.80788259 11.0663146,3.24257445 L4.47482784,8.48488609 C3.82645598,9.00054628 3.71887192,9.94418071 4.23453211,10.5925526 C4.30500305,10.6811601 4.38527899,10.7615046 4.47382636,10.8320511 L4.63,10.9564761 L11.0659024,16.0730648 C11.6126744,16.5077525 12.3871218,16.5074963 12.9336061,16.072447 Z"
                                                          id="Shape" fill="#000000" fill-rule="nonzero"/>
													<path d="M11.0563554,18.6706981 L5.33593024,14.122919 C4.94553994,13.8125559 4.37746707,13.8774308 4.06710397,14.2678211 C4.06471678,14.2708238 4.06234874,14.2738418 4.06,14.2768747 L4.06,14.2768747 C3.75257288,14.6738539 3.82516916,15.244888 4.22214834,15.5523151 C4.22358765,15.5534297 4.2250303,15.55454 4.22647627,15.555646 L11.0872776,20.8031356 C11.6250734,21.2144692 12.371757,21.2145375 12.909628,20.8033023 L19.7677785,15.559828 C20.1693192,15.2528257 20.2459576,14.6784381 19.9389553,14.2768974 C19.9376429,14.2751809 19.9363245,14.2734691 19.935,14.2717619 L19.935,14.2717619 C19.6266937,13.8743807 19.0546209,13.8021712 18.6572397,14.1104775 C18.654352,14.112718 18.6514778,14.1149757 18.6486172,14.1172508 L12.9235044,18.6705218 C12.377022,19.1051477 11.6029199,19.1052208 11.0563554,18.6706981 Z"
                                                          id="Path" fill="#000000" opacity="0.3"/>
												</g>
											</svg>
										</span>
                                        <span class="kt-menu__link-text">Статистика</span>
                                    </router-link>
                                </li>
                                <li class="kt-menu__section ">
                                    <h4 class="kt-menu__section-text">Управление предметами</h4>
                                    <i class="kt-menu__section-icon flaticon-more-v2"></i>
                                </li>
                                <li class="kt-menu__item"  v-bind:class="{'kt-menu__item--active':(page === 'all_items')}" aria-haspopup="true">
                                    <router-link tag="a" :to="{name: 'all_items'}" class="kt-menu__link">
										<span class="kt-menu__link-icon">
											<svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" width="24px" height="24px" viewBox="0 0 24 24" version="1.1" class="kt-svg-icon">
												<g stroke="none" stroke-width="1" fill="none" fill-rule="evenodd">
													<rect id="bound" x="0" y="0" width="24" height="24"/>
													<path d="M12,3 C16.418278,3 20,6.581722 20,11 L20,21 C20,21.5522847 19.5522847,22 19,22 L5,22 C4.44771525,22 4,21.5522847 4,21 L4,11 C4,6.581722 7.581722,3 12,3 Z M9,10 C7.34314575,10 6,11.3431458 6,13 C6,14.6568542 7.34314575,16 9,16 L15,16 C16.6568542,16 18,14.6568542 18,13 C18,11.3431458 16.6568542,10 15,10 L9,10 Z" id="Combined-Shape" fill="#000000"/>
													<path d="M15,14 C14.4477153,14 14,13.5522847 14,13 C14,12.4477153 14.4477153,12 15,12 C15.5522847,12 16,12.4477153 16,13 C16,13.5522847 15.5522847,14 15,14 Z M9,14 C8.44771525,14 8,13.5522847 8,13 C8,12.4477153 8.44771525,12 9,12 C9.55228475,12 10,12.4477153 10,13 C10,13.5522847 9.55228475,14 9,14 Z" id="Combined-Shape" fill="#000000" opacity="0.3"/>
												</g>
											</svg>
										</span>
                                        <span class="kt-menu__link-text">База предметов</span>
                                    </router-link>
                                </li>
                                <li class="kt-menu__item"  v-bind:class="{'kt-menu__item--active':(page === 'styles')}" aria-haspopup="true">
                                    <router-link tag="a" :to="{name: 'styles'}" class="kt-menu__link">
										<span class="kt-menu__link-icon">
											<svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" width="24px" height="24px" viewBox="0 0 24 24" version="1.1" class="kt-svg-icon">
												<g stroke="none" stroke-width="1" fill="none" fill-rule="evenodd">
													<rect id="bound" x="0" y="0" width="24" height="24"/>
													<path d="M12,3 C16.418278,3 20,6.581722 20,11 L20,21 C20,21.5522847 19.5522847,22 19,22 L5,22 C4.44771525,22 4,21.5522847 4,21 L4,11 C4,6.581722 7.581722,3 12,3 Z M9,10 C7.34314575,10 6,11.3431458 6,13 C6,14.6568542 7.34314575,16 9,16 L15,16 C16.6568542,16 18,14.6568542 18,13 C18,11.3431458 16.6568542,10 15,10 L9,10 Z" id="Combined-Shape" fill="#000000"/>
													<path d="M15,14 C14.4477153,14 14,13.5522847 14,13 C14,12.4477153 14.4477153,12 15,12 C15.5522847,12 16,12.4477153 16,13 C16,13.5522847 15.5522847,14 15,14 Z M9,14 C8.44771525,14 8,13.5522847 8,13 C8,12.4477153 8.44771525,12 9,12 C9.55228475,12 10,12.4477153 10,13 C10,13.5522847 9.55228475,14 9,14 Z" id="Combined-Shape" fill="#000000" opacity="0.3"/>
												</g>
											</svg>
										</span>
                                        <span class="kt-menu__link-text">Стили предметов</span>
                                    </router-link>
                                </li>
                                <li class="kt-menu__section ">
                                    <h4 class="kt-menu__section-text">Управление кейсами</h4>
                                    <i class="kt-menu__section-icon flaticon-more-v2"></i>
                                </li>
                                <li class="kt-menu__item"  v-bind:class="{'kt-menu__item--active':(page === 'cases')}" aria-haspopup="true">
                                    <router-link tag="a" :to="{name: 'cases'}" class="kt-menu__link">
										<span class="kt-menu__link-icon">
											<svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" width="24px" height="24px" viewBox="0 0 24 24" version="1.1" class="kt-svg-icon">
												<g stroke="none" stroke-width="1" fill="none" fill-rule="evenodd">
													<rect id="bound" x="0" y="0" width="24" height="24"/>
													<circle id="Oval-5" fill="#000000" opacity="0.3" cx="12" cy="12" r="10"/>
													<path d="M12.4208204,17.1583592 L15.4572949,11.0854102 C15.6425368,10.7149263 15.4923686,10.2644215 15.1218847,10.0791796 C15.0177431,10.0271088 14.9029083,10 14.7864745,10 L12,10 L12,7.17705098 C12,6.76283742 11.6642136,6.42705098 11.25,6.42705098 C10.965921,6.42705098 10.7062236,6.58755277 10.5791796,6.84164079 L7.5427051,12.9145898 C7.35746316,13.2850737 7.50763142,13.7355785 7.87811529,13.9208204 C7.98225687,13.9728912 8.09709167,14 8.21352549,14 L11,14 L11,16.822949 C11,17.2371626 11.3357864,17.572949 11.75,17.572949 C12.034079,17.572949 12.2937764,17.4124472 12.4208204,17.1583592 Z" id="Path-3" fill="#000000"/>
												</g>
											</svg>
										</span>
                                        <span class="kt-menu__link-text">Кейсы</span>
                                    </router-link>
                                </li>
                                <li class="kt-menu__item"  v-bind:class="{'kt-menu__item--active':(page === 'categories')}" aria-haspopup="true">
                                    <router-link tag="a" :to="{name: 'categories'}" class="kt-menu__link">
										<span class="kt-menu__link-icon">
										    <svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" width="24px" height="24px" viewBox="0 0 24 24" version="1.1" class="kt-svg-icon">
												<g stroke="none" stroke-width="1" fill="none" fill-rule="evenodd">
													<rect id="bound" x="0" y="0" width="24" height="24"/>
													<path d="M8,3 L8,3.5 C8,4.32842712 8.67157288,5 9.5,5 L14.5,5 C15.3284271,5 16,4.32842712 16,3.5 L16,3 L18,3 C19.1045695,3 20,3.8954305 20,5 L20,21 C20,22.1045695 19.1045695,23 18,23 L6,23 C4.8954305,23 4,22.1045695 4,21 L4,5 C4,3.8954305 4.8954305,3 6,3 L8,3 Z" id="Combined-Shape" fill="#000000" opacity="0.3"/>
													<path d="M11,2 C11,1.44771525 11.4477153,1 12,1 C12.5522847,1 13,1.44771525 13,2 L14.5,2 C14.7761424,2 15,2.22385763 15,2.5 L15,3.5 C15,3.77614237 14.7761424,4 14.5,4 L9.5,4 C9.22385763,4 9,3.77614237 9,3.5 L9,2.5 C9,2.22385763 9.22385763,2 9.5,2 L11,2 Z" id="Combined-Shape" fill="#000000"/>
													<rect id="Rectangle-152" fill="#000000" opacity="0.3" x="10" y="9" width="7" height="2" rx="1"/>
													<rect id="Rectangle-152-Copy-2" fill="#000000" opacity="0.3" x="7" y="9" width="2" height="2" rx="1"/>
													<rect id="Rectangle-152-Copy-3" fill="#000000" opacity="0.3" x="7" y="13" width="2" height="2" rx="1"/>
													<rect id="Rectangle-152-Copy" fill="#000000" opacity="0.3" x="10" y="13" width="7" height="2" rx="1"/>
													<rect id="Rectangle-152-Copy-5" fill="#000000" opacity="0.3" x="7" y="17" width="2" height="2" rx="1"/>
													<rect id="Rectangle-152-Copy-4" fill="#000000" opacity="0.3" x="10" y="17" width="7" height="2" rx="1"/>
												</g>
											</svg>
										</span>
                                        <span class="kt-menu__link-text">Категории</span>
                                    </router-link>
                                </li>
                                <li class="kt-menu__section ">
                                    <h4 class="kt-menu__section-text">Управление сайтом</h4>
                                    <i class="kt-menu__section-icon flaticon-more-v2"></i>
                                </li>
                                <li class="kt-menu__item" v-bind:class="{'kt-menu__item--active':(page === 'users')}"
                                    aria-haspopup="true">
                                    <router-link tag="a" :to="{name: 'users'}" class="kt-menu__link">
										<span class="kt-menu__link-icon">
											<svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" width="24px" height="24px" viewBox="0 0 24 24" version="1.1" class="kt-svg-icon">
												<g stroke="none" stroke-width="1" fill="none" fill-rule="evenodd">
													<polygon id="Shape" points="0 0 24 0 24 24 0 24"/>
													<path d="M12,11 C9.790861,11 8,9.209139 8,7 C8,4.790861 9.790861,3 12,3 C14.209139,3 16,4.790861 16,7 C16,9.209139 14.209139,11 12,11 Z" id="Mask" fill="#000000" fill-rule="nonzero" opacity="0.3"/>
													<path d="M3.00065168,20.1992055 C3.38825852,15.4265159 7.26191235,13 11.9833413,13 C16.7712164,13 20.7048837,15.2931929 20.9979143,20.2 C21.0095879,20.3954741 20.9979143,21 20.2466999,21 C16.541124,21 11.0347247,21 3.72750223,21 C3.47671215,21 2.97953825,20.45918 3.00065168,20.1992055 Z" id="Mask-Copy" fill="#000000" fill-rule="nonzero"/>
												</g>
											</svg>
										</span>
                                        <span class="kt-menu__link-text">Пользователи</span>
                                    </router-link>
                                </li>
                                <li class="kt-menu__item" v-bind:class="{'kt-menu__item--active':(page === 'promocodes')}"
                                    aria-haspopup="true">
                                    <router-link tag="a" :to="{name: 'promocodes'}" class="kt-menu__link">
										<span class="kt-menu__link-icon">
											<svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" width="24px" height="24px" viewBox="0 0 24 24" version="1.1" class="kt-svg-icon">
												<g stroke="none" stroke-width="1" fill="none" fill-rule="evenodd">
													<rect id="bound" x="0" y="0" width="24" height="24"/>
													<path d="M4,4 L20,4 C21.1045695,4 22,4.8954305 22,6 L22,18 C22,19.1045695 21.1045695,20 20,20 L4,20 C2.8954305,20 2,19.1045695 2,18 L2,6 C2,4.8954305 2.8954305,4 4,4 Z" id="Combined-Shape" fill="#000000" opacity="0.3"/>
													<path d="M18.5,11 L5.5,11 C4.67157288,11 4,11.6715729 4,12.5 L4,13 L8.58578644,13 C8.85100293,13 9.10535684,13.1053568 9.29289322,13.2928932 L10.2928932,14.2928932 C10.7456461,14.7456461 11.3597108,15 12,15 C12.6402892,15 13.2543539,14.7456461 13.7071068,14.2928932 L14.7071068,13.2928932 C14.8946432,13.1053568 15.1489971,13 15.4142136,13 L20,13 L20,12.5 C20,11.6715729 19.3284271,11 18.5,11 Z" id="Path" fill="#000000"/>
													<path d="M5.5,6 C4.67157288,6 4,6.67157288 4,7.5 L4,8 L20,8 L20,7.5 C20,6.67157288 19.3284271,6 18.5,6 L5.5,6 Z" id="Path" fill="#000000"/>
												</g>
											</svg>
										</span>
                                        <span class="kt-menu__link-text">Промокоды</span>
                                    </router-link>
                                </li>
                                <li class="kt-menu__item" v-bind:class="{'kt-menu__item--active':(page === 'seo')}"
                                    aria-haspopup="true">
                                    <router-link tag="a" :to="{name: 'seo'}" class="kt-menu__link">
										<span class="kt-menu__link-icon">
											<svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" width="24px" height="24px" viewBox="0 0 24 24" version="1.1" class="kt-svg-icon">
												<g stroke="none" stroke-width="1" fill="none" fill-rule="evenodd">
													<rect id="bound" x="0" y="0" width="24" height="24"/>
													<path d="M4,4 L20,4 C21.1045695,4 22,4.8954305 22,6 L22,18 C22,19.1045695 21.1045695,20 20,20 L4,20 C2.8954305,20 2,19.1045695 2,18 L2,6 C2,4.8954305 2.8954305,4 4,4 Z" id="Combined-Shape" fill="#000000" opacity="0.3"/>
													<path d="M18.5,11 L5.5,11 C4.67157288,11 4,11.6715729 4,12.5 L4,13 L8.58578644,13 C8.85100293,13 9.10535684,13.1053568 9.29289322,13.2928932 L10.2928932,14.2928932 C10.7456461,14.7456461 11.3597108,15 12,15 C12.6402892,15 13.2543539,14.7456461 13.7071068,14.2928932 L14.7071068,13.2928932 C14.8946432,13.1053568 15.1489971,13 15.4142136,13 L20,13 L20,12.5 C20,11.6715729 19.3284271,11 18.5,11 Z" id="Path" fill="#000000"/>
													<path d="M5.5,6 C4.67157288,6 4,6.67157288 4,7.5 L4,8 L20,8 L20,7.5 C20,6.67157288 19.3284271,6 18.5,6 L5.5,6 Z" id="Path" fill="#000000"/>
												</g>
											</svg>
										</span>
                                        <span class="kt-menu__link-text">Seo</span>
                                    </router-link>
                                </li>
                                <li class="kt-menu__item" v-bind:class="{'kt-menu__item--active':(page === 'settings')}"
                                    aria-haspopup="true">
                                    <router-link tag="a" :to="{name: 'settings'}" class="kt-menu__link">
										<span class="kt-menu__link-icon">
											<svg xmlns="http://www.w3.org/2000/svg"
                                                 xmlns:xlink="http://www.w3.org/1999/xlink" width="24px" height="24px"
                                                 viewBox="0 0 24 24" version="1.1" class="kt-svg-icon">
												<g stroke="none" stroke-width="1" fill="none" fill-rule="evenodd">
													<rect id="bound" x="0" y="0" width="24" height="24"/>
													<path d="M18.6225,9.75 L18.75,9.75 C19.9926407,9.75 21,10.7573593 21,12 C21,13.2426407 19.9926407,14.25 18.75,14.25 L18.6854912,14.249994 C18.4911876,14.250769 18.3158978,14.366855 18.2393549,14.5454486 C18.1556809,14.7351461 18.1942911,14.948087 18.3278301,15.0846699 L18.372535,15.129375 C18.7950334,15.5514036 19.03243,16.1240792 19.03243,16.72125 C19.03243,17.3184208 18.7950334,17.8910964 18.373125,18.312535 C17.9510964,18.7350334 17.3784208,18.97243 16.78125,18.97243 C16.1840792,18.97243 15.6114036,18.7350334 15.1896699,18.3128301 L15.1505513,18.2736469 C15.008087,18.1342911 14.7951461,18.0956809 14.6054486,18.1793549 C14.426855,18.2558978 14.310769,18.4311876 14.31,18.6225 L14.31,18.75 C14.31,19.9926407 13.3026407,21 12.06,21 C10.8173593,21 9.81,19.9926407 9.81,18.75 C9.80552409,18.4999185 9.67898539,18.3229986 9.44717599,18.2361469 C9.26485393,18.1556809 9.05191298,18.1942911 8.91533009,18.3278301 L8.870625,18.372535 C8.44859642,18.7950334 7.87592081,19.03243 7.27875,19.03243 C6.68157919,19.03243 6.10890358,18.7950334 5.68746499,18.373125 C5.26496665,17.9510964 5.02757002,17.3784208 5.02757002,16.78125 C5.02757002,16.1840792 5.26496665,15.6114036 5.68716991,15.1896699 L5.72635306,15.1505513 C5.86570889,15.008087 5.90431906,14.7951461 5.82064513,14.6054486 C5.74410223,14.426855 5.56881236,14.310769 5.3775,14.31 L5.25,14.31 C4.00735931,14.31 3,13.3026407 3,12.06 C3,10.8173593 4.00735931,9.81 5.25,9.81 C5.50008154,9.80552409 5.67700139,9.67898539 5.76385306,9.44717599 C5.84431906,9.26485393 5.80570889,9.05191298 5.67216991,8.91533009 L5.62746499,8.870625 C5.20496665,8.44859642 4.96757002,7.87592081 4.96757002,7.27875 C4.96757002,6.68157919 5.20496665,6.10890358 5.626875,5.68746499 C6.04890358,5.26496665 6.62157919,5.02757002 7.21875,5.02757002 C7.81592081,5.02757002 8.38859642,5.26496665 8.81033009,5.68716991 L8.84944872,5.72635306 C8.99191298,5.86570889 9.20485393,5.90431906 9.38717599,5.82385306 L9.49484664,5.80114977 C9.65041313,5.71688974 9.7492905,5.55401473 9.75,5.3775 L9.75,5.25 C9.75,4.00735931 10.7573593,3 12,3 C13.2426407,3 14.25,4.00735931 14.25,5.25 L14.249994,5.31450877 C14.250769,5.50881236 14.366855,5.68410223 14.552824,5.76385306 C14.7351461,5.84431906 14.948087,5.80570889 15.0846699,5.67216991 L15.129375,5.62746499 C15.5514036,5.20496665 16.1240792,4.96757002 16.72125,4.96757002 C17.3184208,4.96757002 17.8910964,5.20496665 18.312535,5.626875 C18.7350334,6.04890358 18.97243,6.62157919 18.97243,7.21875 C18.97243,7.81592081 18.7350334,8.38859642 18.3128301,8.81033009 L18.2736469,8.84944872 C18.1342911,8.99191298 18.0956809,9.20485393 18.1761469,9.38717599 L18.1988502,9.49484664 C18.2831103,9.65041313 18.4459853,9.7492905 18.6225,9.75 Z"
                                                          id="Combined-Shape" fill="#000000" fill-rule="nonzero"
                                                          opacity="0.3"/>
													<path d="M12,15 C13.6568542,15 15,13.6568542 15,12 C15,10.3431458 13.6568542,9 12,9 C10.3431458,9 9,10.3431458 9,12 C9,13.6568542 10.3431458,15 12,15 Z"
                                                          id="Path" fill="#000000"/>
												</g>
											</svg>
										</span>
                                        <span class="kt-menu__link-text">Настройки</span>
                                    </router-link>
                                </li>
                            </ul>
                        </div>
                    </div>
                </div>

                <div class="kt-grid__item kt-grid__item--fluid kt-grid kt-grid--hor kt-wrapper" id="kt_wrapper">
                    <div id="kt_header" class="kt-header kt-grid__item  kt-header--fixed ">
                        <button class="kt-header-menu-wrapper-close" id="kt_header_menu_mobile_close_btn"><i
                                class="la la-close"></i></button>
                        <div class="kt-header-menu-wrapper" id="kt_header_menu_wrapper">

                        </div>

                        <div class="kt-header__topbar">
                            <div class="kt-header__topbar-item kt-header__topbar-item--user">
                                <div class="kt-header__topbar-wrapper" data-toggle="dropdown" data-offset="0px,0px">
                                    <div class="kt-header__topbar-user">
                                        <span class="kt-header__topbar-welcome kt-hidden-mobile">Привет,</span>
                                        <span class="kt-header__topbar-username kt-hidden-mobile">{{$root.user.username}}</span>
                                        <img alt="Pic" :src="$root.user.avatar"/>
                                    </div>
                                </div>
                                <div class="dropdown-menu dropdown-menu-fit dropdown-menu-right dropdown-menu-anim dropdown-menu-top-unround dropdown-menu-xl">
                                    <div class="kt-user-card kt-user-card--skin-dark kt-notification-item-padding-x"
                                         style="background-image: url(/dash/img/bg-1.jpg)">
                                        <div class="kt-user-card__avatar">
                                            <img alt="Pic" :src="$root.user.avatar"/>
                                        </div>
                                        <div class="kt-user-card__name">
                                            {{ $root.user.username }}
                                        </div>
                                    </div>
                                    <div class="kt-notification">
                                        <a href="/admin/user/" class="kt-notification__item">
                                            <div class="kt-notification__item-icon">
                                                <i class="flaticon2-calendar-3 kt-font-success"></i>
                                            </div>
                                            <div class="kt-notification__item-details">
                                                <div class="kt-notification__item-title kt-font-bold">
                                                    Мой профиль
                                                </div>
                                                <div class="kt-notification__item-time">
                                                    Настройки Вашего аккаунта
                                                </div>
                                            </div>
                                        </a>
                                        <div class="kt-notification__custom">
                                            <a href="/" class="btn btn-label-brand btn-sm btn-bold">Вернуться на
                                                сайт</a>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                    <div class="kt-grid__item kt-grid__item--fluid kt-grid kt-grid--hor">
                        <router-view></router-view>
                    </div>

                    <div class="kt-footer kt-grid__item kt-grid kt-grid--desktop kt-grid--ver-desktop">
                        <div class="kt-footer__copyright">
                            2019 © Сайт разработан пользователем ArtourBabaev
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <div id="kt_scrolltop" class="kt-scrolltop">
            <i class="fa fa-arrow-up"></i>
        </div>
    </div>
</template>

<script>
    import axios from 'axios';

    export default {
        data() {
            return {
                page: null
            }
        },
        beforeMount() {
            this.page = this.$router.currentRoute.name;
        },
        beforeUpdate() {
            this.page = this.$router.currentRoute.name;
        },
        methods: {
            async socketRun() {
                $.wnoty({
                    type: 'info',
                    message: 'Запускаем сокет'
                })

                const request = await axios.post('/api/admin/settings/socketRun');
                const data = request.data;

                $.wnoty({
                    type: data.type,
                    message: data.message
                })
            },
            async socketOff() {
                $.wnoty({
                    type: 'info',
                    message: 'Выключаем сокет'
                })

                const request = await axios.post('/api/admin/settings/socketOff');
                const data = request.data;

                $.wnoty({
                    type: data.type,
                    message: data.message
                })
            }
        }
    }
</script>