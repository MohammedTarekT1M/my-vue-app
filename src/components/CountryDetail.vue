<div class="col-12 col-md-6">
                <h2>Selected Countries</h2>
                <ul class="list-group">
                    <li class="list-group-item">
                        {{selectedCountry.id}}
                    </li>
                    <li class="list-group-item">
                        <img :src="(selectedCountry.img)" class="img-fluid" />
                    </li>
                    <li class="list-group-item">
                        {{selectedCountry.name}}
                    </li>
                    <li class="list-group-item">
                        {{selectedCountry.capital}}
                    </li>
                    <li class="list-group-item">
                        <details>
                            <summary>more info</summary>
                            {{selectedCountry.details}}
                        </details>
                    </li>
                    <li class="list-group-item">
                        {{selectedCountry.cost}}
                    </li>
                    <li v-if="isExpensive" class="list-group-item pt-3">
                        <p class="bg-danger text-white">DUUR</p>
                    </li>
                </ul>
            </div>
            <CountryDetail v-if="selectedCountry" :country="selectedCountry"/>

            <script>
            export default {
                name : "VacationPicker",
                props: ['country'],                
            }
            </script>