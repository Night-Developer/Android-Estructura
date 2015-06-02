# Android-Estructura
Estructura de projecto de archivo de una aplicacion android y un modelo async para llamadas HTTP


#Estructura de folder

    App
        Domain
            DAO
        Views
            Fragments
            Adapters
        Data
            Network
                UtilObjects
                    CallbackView.class
                    GenericRunner.class
                    AsyncGeneric.class
                WebServiceClient.class
            Parsers
            Handlers
            DataFacade.class
        AplicationClass.class
    
#CallbackView
    class CallBackView{
        public void backToView(List<Items> result){
        }
    }

#GenericRunner
    public abstract class RunnerGeneric {
        public abstract void run();
 
        public void postExecute(){
        }
    }

#AsyncGeneric
    public class AsyncGeneric extends AsyncTask<Void, Void, Void> {
        private AsyncGeneric(){
        }
 
        public static AsyncGeneric getInstance(){
            instance = new AsyncGeneric();
            return instance;
        }
 
        @Override
        protected Void doInBackground(Void... params) {
        }
 
        @Override
        protected void onPostExecute(Void result) {
        }
    }

