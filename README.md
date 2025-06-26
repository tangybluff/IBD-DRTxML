<img src="https://formacionmassalud.iavante.es/pluginfile.php/1/theme_edumy/headerlogo2/1722409266/logo-web-fps-718x150%20v2%20copia.png" alt="Fundación Progreso y salud" style="float: right; width: 200px; height: auto; margin-left: 10px;">

# IBD DRTxML

## FPS-EII-2021-04
Development and validation of Machine Learning models to predict medium and long-term clinical remission in patients with Crohn's disease and ulcerative colitis (UC) undergoing treatment with vedolizumab or ustekinumab.

## Summary

This project is a collaborative effort between the Big Data Department of the Andalusian Public Foundation for Progress and Health and the Virgen Macarena University Hospital. Its primary objective is to develop and validate machine learning models that predict medium- and long-term clinical outcomes in patients with Crohn's disease and ulcerative colitis (UC) treated with vedolizumab or ustekinumab. By leveraging routinely collected clinical data available prior to the initiation of biological therapy, the project seeks to build a clinical decision support system capable of forecasting clinical response at 26 and 52 weeks, as well as clinical remission at 52 weeks.

The predictive models will help clinicians identify patients most likely to benefit from these treatments, optimize resource allocation, and personalize disease management strategies. The analysis will focus on determining the most influential variables for predicting treatment outcomes and understanding how these factors contribute to positive or negative responses.

In addition to analyzing the overall patient cohort, the study will stratify patients into subcohorts based on medication type and disease classification. Predictive models will be developed and evaluated for each subcohort, enabling more tailored and precise predictions for specific patient groups. Ultimately, the project aims to enhance clinical decision-making and improve long-term outcomes for individuals with inflammatory bowel disease.

## Inclusion / Exclusion Criteria

The study population comprises individuals from the Andalusian Public Health System within the service area of the Virgen Macarena University Hospital (HUVM). Eligible participants must fulfill all inclusion criteria and not meet any exclusion criteria:

**Inclusion criteria:**

- Be of legal age (>18 years).
- Coded diagnosis of moderate-to-severe Crohn's disease or Ulcerative Colitis.
- Currently receiving or having previously received treatment with ustekinumab and/or vedolizumab.

**Exclusion criteria:**

- Unavailable and/or lack of access to electronic health record data.
- Fewer than 50% of required study variables documented.
- Loss to follow-up before 26 weeks after initiation of treatment.

## Variables

Only a subset of variables is included in the predictive models. Selection is based on clinical criteria with strong association with the target outcomes, as determined by expert consensus and data-driven analysis.

### Independent
| Name | Type | Units | Description |
| --- | --- | --- | --- |
| ID | Text | - | Unique anonymized patient identifier. |
| fecha_inicio_far | Date | dd/mm/yyyy | Date when the patient started the biological drug treatment. |
| fecha_diag | Date | dd/mm/yyyy | Date of initial diagnosis of inflammatory bowel disease (IBD). |
| ppio_activo | Factor | - | Biological drug administered:<br>USTEKINUMAB<br>VEDOLIZUMAB |
| sexo | Factor | - | Patient's biological sex. |
| familia_eii | Factor | - | Family history of IBD:<br>None (0)<br>First-degree relative (1)<br>Second-degree relative (2) |
| loc_ec | Factor | - | Crohn's disease location:<br>Other disease (0)<br>Ileal (1)<br>Colonic (2)<br>Ileocolonic (3)<br>Ileocolonic + upper GI (4)<br>Ileal + upper GI (5) |
| comp_ec | Factor | - | Crohn's disease behavior:<br>Other disease (0)<br>Inflammatory (1)<br>Stenosing (2)<br>Fistulizing (3) |
| exten_cu | Factor | - | Ulcerative colitis extent:<br>Other disease (0)<br>Proctitis (1)<br>Left-sided colitis (2)<br>Pancolitis (3) |
| tipo_eii | Factor | - | Type of IBD:<br>Crohn's Disease (CD)<br>Ulcerative Colitis (UC) |
| preianal | Factor | - | History of recurrent perianal fistulas:<br>Yes (1)<br>No (0) |
| ada_previo | Factor | - | Prior treatment with Adalimumab (anti-TNF):<br>Yes (1)<br>No (0) |
| ifx_previo | Factor | - | Prior treatment with Infliximab (anti-TNF):<br>Yes (1)<br>No (0) |
| uste_previo | Factor | - | Prior treatment with Ustekinumab (biologic):<br>Yes (1)<br>No (0) |
| vedo_previo | Factor | - | Prior treatment with Vedolizumab (biologic):<br>Yes (1)<br>No (0) |
| tofa_previo | Factor | - | Prior treatment with Tofacitinib (biologic):<br>Yes (1)<br>No (0) |
| certol_previo | Factor | - | Prior treatment with Certolizumab (biologic):<br>Yes (1)<br>No (0) |
| golim_previo | Factor | - | Prior treatment with Golimumab (biologic):<br>Yes (1)<br>No (0) |
| cx_previa_eii | Factor | - | History of IBD-related surgery before starting the drug:<br>Yes (1)<br>No (0) |
| tabaco | Factor | - | Smoking status at treatment initiation:<br>Non-smoker (0)<br>Smoker (1)<br>Ex-smoker (2) |
| meis_espondiloartropatías | Factor | - | Presence of spondyloarthropathies (extraintestinal manifestation):<br>Present (1)<br>Not present (0) |
| meis_uveitis | Factor | - | Presence of uveitis (extraintestinal manifestation):<br>Present (1)<br>Not present (0) |
| meis_eritema_nodoso | Factor | - | Presence of erythema nodosum (extraintestinal manifestation):<br>Present (1)<br>Not present (0) |
| meis_pioderma_gangrenoso | Factor | - | Presence of pyoderma gangrenosum (extraintestinal manifestation):<br>Present (1)<br>Not present (0) |
| meis_colangitis_esclerosanteprimaria | Factor | - | Presence of primary sclerosing cholangitis (extraintestinal manifestation):<br>Present (1)<br>Not present (0) |
| meis_estomatitis_aftosa | Factor | - | Presence of aphthous stomatitis (extraintestinal manifestation):<br>Present (1)<br>Not present (0) |
| meis_SdSweet | Factor | - | Presence of Sweet’s syndrome (extraintestinal manifestation):<br>Present (1)<br>Not present (0) |
| meis_psoriasis | Factor | - | Presence of psoriasis (extraintestinal manifestation):<br>Present (1)<br>Not present (0) |
| meis_hidrosiadenitis | Factor | - | Presence of hidradenitis (extraintestinal manifestation):<br>Present (1)<br>Not present (0) |
| meis_vasculitis | Factor | - | Presence of vasculitis (extraintestinal manifestation):<br>Present (1)<br>Not present (0) |
| meis_vitiligo | Factor | - | Presence of vitiligo (extraintestinal manifestation):<br>Present (1)<br>Not present (0) |
| meis_osteoporosis | Factor | - | Presence of osteoporosis (extraintestinal manifestation):<br>Present (1)<br>Not present (0) |
| meis_fenom_tromboembolico | Factor | - | Presence of thromboembolic events (extraintestinal manifestation):<br>Present (1)<br>Not present (0) |
| edad_inicio_far | Integer | Years | Age of the patient at the start of biological drug treatment. |
| edad_diag | Integer | Years | Age of the patient at the time of IBD diagnosis. |
| cort_12m_previo | Factor | - | Use of corticosteroids in the 12 months prior to starting the drug:<br>Yes (1)<br>No (0) |
| diabetes | Factor | - | Diagnosis of diabetes at treatment initiation:<br>Yes (1)<br>No (0) |
| asma | Factor | - | Diagnosis of asthma at treatment initiation:<br>Yes (1)<br>No (0) |
| vih | Factor | - | Diagnosis of HIV at treatment initiation:<br>Yes (1)<br>No (0) |
| migrana | Factor | - | Diagnosis of migraine at treatment initiation:<br>Yes (1)<br>No (0) |
| calprotectina | Continuous | µg/g | Fecal calprotectin level measured within 8 weeks before or at the start of treatment. |
| lab_velocidad_sed_globular | Continuous | mm/h | Erythrocyte sedimentation rate (ESR) in whole blood. |
| lab_sodio | Continuous | mEq/L | Serum sodium concentration. |
| lab_aspartato_transaminasa | Integer | U/L | Serum aspartate transaminase (AST) enzyme activity. |
| lab_glucosa | Continuous | mg/dL | Serum glucose concentration. |
| lab_proteinas_totales | Continuous | g/dL | Total serum protein concentration. |
| lab_urea | Continuous | mg/dL | Serum urea concentration. |
| lab_potasio | Continuous | mEq/L | Serum potassium concentration. |
| lab_fosfato | Continuous | mg/dL | Serum phosphate concentration. |
| lab_proteina_C | Continuous | mg/L | Serum C-reactive protein (CRP) concentration. |

### Dependent

| Name | Type | Units | Description |
| --- | --- | --- | --- |
| id_paciente | Text | - | Anonymized patient identifier. |
| remision_clinica_26s | Factor | - | Indicates whether clinical remission was achieved 26 weeks after starting the biological treatment:<br><br>Achieved (1)<br>Not achieved (0) |
| remision_clinica_52s | Factor | - | Indicates whether clinical remission was achieved 52 weeks after starting the biological treatment:<br><br>Achieved (1)<br>Not achieved (0) |
| respuesta_clinica_26s | Factor | - | Indicates whether a clinical response was achieved 26 weeks after starting the biological treatment:<br><br>Achieved (1)<br>Not achieved (0) |
| respuesta_clinica_52s | Factor | - | Indicates whether a clinical response was achieved 52 weeks after starting the biological treatment:<br><br>Achieved (1)<br>Not achieved (0) |
**Note:**  
For the development and evaluation of predictive models, only the following target variables will be used:

- `respuesta_clinica_26s`: Clinical response at 26 weeks
- `respuesta_clinica_52s`: Clinical response at 52 weeks
- `remision_clinica_52s`: Clinical remission at 52 weeks

These variables represent the primary clinical outcomes of interest for model training and validation.